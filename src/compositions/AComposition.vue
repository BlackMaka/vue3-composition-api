<template>
  <div
    v-bind="$attrs"
    @click="helloMethod">
    <slot></slot>
  </div>
</template>

<script>
import { onMounted } from 'vue';
export default {
  inheritAttrs:false,
  props:{
    color:{
      type:String,
      default:'gray'
    }
  },
  emits:['hello'],
  setup(props, context){
      function helloMethod(){
          context.emit('hello');
      }
      onMounted(()=>{
          console.log(props.color);
          console.log(context.attrs);
      })
      
      return{
          helloMethod
      }
  }

}
</script>

<style>

</style>