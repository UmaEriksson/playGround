<template>
  
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <toDO/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import toDO from './components/toDO.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    toDO
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
 
}
</style>
