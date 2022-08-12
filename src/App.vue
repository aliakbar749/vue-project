<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Navbar></Navbar>
    <Hook></Hook>
  </div>
</template>

<script>

import Navbar from './components/Navbar.vue'
import Hook from './components/Hook.vue'


export default {
  name: 'App',
  components: {
    Navbar,
    Hook
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
