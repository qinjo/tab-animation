<template>
  <div id="app">
    <Tab/>
  </div>
</template>
  
  
<script setup lang='ts'>
import Tab from './components/tab/index.vue';
defineOptions({
  name: 'App'
})
</script>
<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
}
</style>