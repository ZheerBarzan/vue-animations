<script setup>
import { ref } from 'vue';

const showText = ref(true)
</script>

<template>
  <main>

    <div class="container">
      <Transition name="fade">
      <h1 v-if="showText">hello world</h1>
      <h1 v-else>good bye world</h1>
    
    </Transition>
    </div>

    <button @click="showText = !showText">toggle</button>
  </main>
</template>

<style scoped>
.fade-enter-from{
opacity: 0;}
.fade-enter-to{
opacity: 1;}
.fade-enter-active{
  transition: all 1s ease;
}
.fade-leave-from{
opacity: 1;}
.fade-leave-to{
opacity: 0;}
.fade-leave-active{
  transition: all 1s ease;
}
.container{
  position: relative;
  
}
h1{
  position: absolute;
}
button{
  margin-top: 50px;
}
</style>