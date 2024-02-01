<!-- (24-02-01-thu) -->

<template>
  <label>선택: <input type="checkbox" true-value="yes" false-value="no" v-model="checked"></label>
  <p>선택값: {{checked}}</p>

  <lavel>text속성: <input type="text" v-bind:value="ival"></lavel><!-- v-model의 인풋 타입이 텍스트면 => value라는 속성에 바인딩 됨. -->
  <p>값: {{ival}}</p>

  <!-- v-bind: attribute의 값을 바인딩할 때 쓰임 -->
  <img v-bind:src="imgSrc" v-bind:width="imgWidth"> <!-- v-bind:width= 여기서 :width= 이렇게만 써도 됨(v-bind 생략 가능) -->
  <input type="text" v-model="textStr">
  <button v-bind:disabled="textStr == ''">Click</button>

</template>

<script>
export default {
    data(){
      return{        
        checked: 'yes',
        ival: 'sample',
        checkVal: true,
        imgSrc: 'https://kr.vuejs.org/images/logo.png',
        imgWidth: '100px',
        isTrue: true,
        textStr: ''
      }
    }    
}
</script>

<style>
</style>