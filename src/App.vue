<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <HelloWorld/> -->
    <h5tmp/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import h5tmp from './components/h5tmp'

export default {
  name: 'app',
  components: {
    HelloWorld,
    h5tmp
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
