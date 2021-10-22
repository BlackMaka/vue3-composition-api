<template>
  <h1 @click="add">
    {{ count }}
  </h1>
</template>

<script>
import {ref} from 'vue';
export default {
  setup(){
      //컴포지션 반응성 추가 ref
      let count = ref(0);
      function add(){
          count.value +=1;
      }
      return{
          count,
          add
      }
  }
}
</script>

<style>

</style>