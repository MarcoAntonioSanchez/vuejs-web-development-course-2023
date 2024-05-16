<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1 class="test">Test</h1>
  <TestClass />
</template>

<script>
import TestClass from './components/Class.vue';

export default {
  name: 'App',
  components: {
    TestClass,
  },
};
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
.test {
  background-color: red;
}
</style>
