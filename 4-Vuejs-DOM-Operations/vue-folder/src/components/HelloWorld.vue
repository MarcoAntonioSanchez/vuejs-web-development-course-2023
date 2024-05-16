<template>
  <div>
    <!-- One way to bind a method on click in the button tag -->
    <!-- <button v-on:click="handleClick">Click</button> -->
    <!-- Alternative way to bind a method on click in the button tag -->
    <!-- <button @click="handleClick">Click</button>
    <h1 id="header">Header</h1> -->
    <!-- <h1>{{ msg }}</h1> -->
    <!-- <button @click="handleClick">Click</button> -->
    <!-- Set 100 value as param for the handleClick2 function -->
    <!-- <button @click="handleClick2(100)">Click</button> -->
    <form @submit.prevent="handleSubmit">
      <input type="text"><br>
      <button type="submit">Submit</button>
    </form>
    <button @click.once="onBtnClick">Inc</button>
    <p>{{ number }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: { // You can add methods / functions to provide custom functionallity to the components structure like HTML tags
    handleClick(event){
      console.log(event);
      event.target.style.backgroundColor="red"; // Using the event.target to specify the HTML tag
    },
    handleClick2(param){
      console.log("PARAM",param); // Printing the assigned param to the click event
    },
    handleSubmit() {
      console.log("Form Submitted");
    },
    onBtnClick() {
      this.number=this.number + 1;
    }
  },
  data() {
    return {
      number: 1,
    };
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
