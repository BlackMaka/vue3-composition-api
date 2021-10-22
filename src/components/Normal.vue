<template>
  <h1 @click="add">
    {{ count }}
  </h1>
</template>

<script>
export default {
  data(){
    return{
      count:0,
    }
  },
  methods:{
    add(){
      this.count += 1;
    }
  }
}
</script>

<style>

</style>