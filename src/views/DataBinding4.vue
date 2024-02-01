<!-- (24-02-01-thu) -->

<template>
  <div class="container" v-bind:class="simpleClass">
    집에 가자
  </div>
  <div class="container" v-bind:class="{active: activeValue, 'text-red': redValue}">
    얼른 마치고 집에 가자
  </div>
  <div class="container" v-bind:class="[activeClass, redClass]">
    지금은 5교시
  </div>
  <div style="color: red; background: yellow;">
    style1
  </div>
  <div v-bind:style="{color: att1, background: att2}">
    style2
  </div>
  <div v-bind:style="colorStyle">
    style3
  </div>
</template>

<script>
export default {
  data() {
    return {
      simpleClass: 'active text-red',
      activeValue: true,
      redValue: false,
      activeClass: 'active',
      redClass: 'text-red',
      att1: 'red',
      att2: 'skyblue',
      //colorStyle: 'color: red; background: grey' // 첫번째 방식
      colorStyle: {
        color: 'red',
        background: 'pink'
      }
    };
  },
  beforeMouted(){
    console.log('1', this.att1)
  },
  mouted(){
    console.log(this)
  },
  methods: { //이벤트 실행함수

  }
};
</script>

<style>
.container {
  width: 100%;
  height: 50px;
}
.active {
  background-color: yellowgreen;
  font-weight: bold;
}
.text-red {
  color: red;
}
</style>