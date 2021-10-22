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
import { ref, computed, watch, onMounted } from 'vue';
export default {
    setup(){
        const count = ref(0);
        function add(){
            count.value += 1;
        }
        const dblCount = computed(()=>{
            return count.value * 2;
        });
        
        const message = ref('Hello');
        function changeMsg(){
            message.value = 'Good';
        }
        const reversedMessage = computed(()=>{
            return message.value.split('').reverse().join('');
        });

        watch( message, (newValue) =>{
            console.log(`newValue : ${newValue}`);
        })
        onMounted(()=>{
            console.log(`mounted : ${count.value}`);
        })
        //created()
        console.log(`created : ${message.value}`);
        return{
            count,
            dblCount,
            add,
            message,
            reversedMessage,
            changeMsg
        }
    }
}
</script>

<style>

</style>