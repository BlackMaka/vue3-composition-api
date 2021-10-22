<template>
  <div @click="add">
    {{ count }} - {{ dblCount }}
  </div>
  <button @click="changeMsg">
    buttttton
  </button>
  <div>
    {{ message }} - {{ reversedMessage }}
  </div>
</template>

<script>
export default {
  data(){
    return {
      count:0,
      message:"abcde"
    }
  },
  computed:{
    dblCount(){
      return this.count * 2;
    },
    reversedMessage(){
      return this.message.split('').reverse().join('');
    }
  },
  mounted(){
    console.log(this.message);
  },
  created(){
    console.log(this.count);
  },
  watch:{
    message(newValue, oldValue){
      console.log(`newValue : ${ newValue }, oldVAlue:${oldValue}`);
    }
  },
  methods:{
    add(){
      this.count += 1;
    },
    changeMsg(){
      this.message = 'Helelelel';
    }
  }
}
</script>

<style>

</style>