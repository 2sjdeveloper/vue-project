<!-- (24-02-01-thu) -->

<template>
  <div>
    <h1>{{ `${lastName} / ${firstName}` }}</h1>
    <h1>{{ `${fullName}` }}</h1>
  </div>
  <input type="text" v-model="firstName" />
</template>

<script>
export default {
  data() {
    return {
      firstName: "kildong",
      lastName: "Hong",
    };
  },
  computed: { //복합데이터처리
    fullName() {
      return `${this.lastName} - ${this.firstName}`;
    },
  },
  watch: { //데이터 변경 이전, 이후에 어떤 처리를 하고싶을 경우.
    firstName(curr, bef){ //curr : 변경후의 값, bef : 변경전의 값
      console.log(curr, bef); 
    }
  }
};
</script>