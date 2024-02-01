<!-- (24-02-01-thu) -->

<template>
  <h3>Hello?, {{msg}}</h3>    
  <div>{{htmlStr}}</div>
  <div v-html="htmlStr"></div>
  <input type="text" v-model="vmodel" />
  <p>{{vmodel}}</p>
  <textarea cols="30" rows="10" v-model="message"></textarea>
</template>

<script>
export default {
    data(){
      return{
        msg: '오늘점심뭐야',
        htmlStr: '<p style="color: red;">하다보면 되것지 화이팅. 근데 쉬는시간은 언제.. </p>',
        vmodel: '세상에 아직 26분이나 남았음',
        message: '집에 가고 싶어여.\n 집에 언제감..?\n 아직 밥도 안먹었음 심지어 ㅠㅠ '

      }
    }
}
</script>

<style>

</style>