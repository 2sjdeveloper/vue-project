<!-- (24-02-01-thu) -->

<template>
  <div class="about">
    <button v-on:click="increaseCounter">Add 1</button>
    <p>Counter is : {{ counter }}</p>
    <button v-on:click="increaseCounter2(3)">Increase</button>
    <button v-on:click="one(), two()">다중호출</button>

    <select v-model="city" v-on:change="changeSelect">
      <option value="1">서울은 서울서울</option>
      <option value="2">부산은 끼룩끼룩</option>
      <option value="3">제주는 혼자옵서예</option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 5,
      city: "1",
    };
  },
  methods: {
    increaseCounter() {
      console.log("increaseCounter");
      this.counter = this.counter + parseInt(this.city);
    },
    increaseCounter2(num) {
      this.counter = this.counter + num;
    },
    one() {
      alert("one");
    },
    two() {
      alert("two");
    },
    changeSelect() {
      alert(this.city);
    },
  },
  beforeUpdate() {
    //화면에 변경이 생기기 전에 필요한 처리를 구현
    console.log("beforeUpdate");
  },
  updated() {
    //화면에 변경이 생긴 후에 필요한 처리를 구현
    console.log("updated");
  },
};
</script>