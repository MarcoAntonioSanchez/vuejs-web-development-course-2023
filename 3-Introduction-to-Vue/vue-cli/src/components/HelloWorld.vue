<template>
  <div class="hello">Hello Vue.js</div>
  <div style="color:blue;background-color:black;padding:20px;">Hello Vue.js2</div>
  <div>{{ msg }}</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: {
      type: String,
      required: true,
      default: 'This is a default message',
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
