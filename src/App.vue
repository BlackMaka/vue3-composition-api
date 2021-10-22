<template>
  <!-- <Normal
    class="heropy"
    style="color:red"
    color="#ff0000"
    @hello="log">
    Apple
  </Normal> -->
  <ACV
    class="heropy"
    style="color:red"
    color="#ff0000"
    @hello="log">
    ACV
  </ACV>
</template>

<script>
//import Normal from '~/components/Normal';
import ACV from '~/compositions/AComposition';
export default {
  components:{
    //Normal,
    ACV
  },
  methods:{
    log(){
      console.log('Hellog');
    }
  }
}
</script>

<style>

</style>