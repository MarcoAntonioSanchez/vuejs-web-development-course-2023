<!-- HTML -->
<!-- template tags are use for structuring the Vue.js components -->
<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<!-- JavaScript -->
<!-- script tags provides functionallity to the component -->
<!-- the script tags process and display data -->
<!-- you can add some event handling too -->
<!-- ROUTER DEFINITION -->
<!-- helps with the navigation through the SPA (Vue.js app) -->
<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<!-- CSS -->
<!-- Styling components with HTML and CSS, as always -->
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