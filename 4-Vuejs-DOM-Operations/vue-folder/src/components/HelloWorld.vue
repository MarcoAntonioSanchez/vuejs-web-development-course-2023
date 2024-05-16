<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
    <h1>{{ gender }}</h1>
    <h1>{{ "Hello" }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      name: "Jhon",
      age: 25,
      gender: true,
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
