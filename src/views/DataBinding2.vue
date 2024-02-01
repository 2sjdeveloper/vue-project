<!-- (24-02-01-thu) -->

<template>
  <select v-model="city">
    <option value="02">서울은 케텍스</option>
    <option value="03">부산은 자동차</option>
    <option value="04">제주도는 비행기</option>
  </select>
  <label>선택: <input type="checkbox" true-value="yes" false-value="no" v-model="checked"></label>
  <p>선택값: {{checked}}</p>

<label><input type="checkbox" v-model="checkItems" value="01">서울은 서울서울</label>
<label><input type="checkbox" v-model="checkItems" value="02">부산은 끼룩끼룩</label>
<label><input type="checkbox" v-model="checkItems" value="01">제주도는 혼저옵서예</label>
<label><input type="checkbox" v-model="checkItems" value="02">대전은 성심당</label>
<label><input type="checkbox" v-model="checkItems" value="03">대구는 대프리카</label>
  <p>선택값: {{checkItems}}</p>
</template>

<script>
export default {
    data(){
      return{
        city: '04',
        checked: 'yes',
        checkItems: ['01']
        
      }
    }    
}
</script>

<style>
</style>