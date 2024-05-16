<template>
  <div>
    <!-- One way to bind a method on click in the button tag -->
    <!-- <button v-on:click="handleClick">Click</button> -->
    <!-- Alternative way to bind a method on click in the button tag -->
    <!-- <button @click="handleClick">Click</button>
    <h1 id="header">Header</h1> -->
    <h1>{{ msg }}</h1>
    <button @click="handleClick">Click</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: { // You can add methods / functions to provide custom functionallity to the components structure like HTML tags
    handleClick(event){
      console.log(event);
      event.target.style.backgroundColor="red"; // Using the event.target to specify the HTML tag
    }
  },
  data() {
    return {};
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
