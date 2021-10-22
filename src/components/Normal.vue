<template>
  <div
    v-bind="$attrs"
    @click="helloMethod">
    <slot></slot>
  </div>
</template>

<script>
export default {
  inheritAttrs:false,
  props:{
    color:{
      type:String,
      default:'gray'
    }
  },
  emits:['hello'],
  mounted(){
    console.log(this.$attrs);
    console.log(this.color);
  },
  methods:{
    helloMethod(){
      this.$emit('hello');
    }
  }

}
</script>

<style>

</style>