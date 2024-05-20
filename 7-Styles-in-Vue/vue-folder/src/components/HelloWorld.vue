<template>
  <!--
    <div>
    :CLASS
    Binding example
    <div :class="className">
      Hello
    </div>
    :CLASS + { active: }
    Alternative binding example, check if both attributes are true, so the calss is binded
    <h1 :class="{ active:isActive,back:isActive }">hello</h1>
  </div>
  -->
  <div>
  <!-- Bindigng example, using an array for multiple classes -->
    <h1 :class="[a, b]">Hello</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {},
  data() {
    return {
      isActive: true, // If this is true, the color will be blue, otherwise will be default's black
      className: "color-blue", // For the 1st classes binding exmaple.
      a: "A", // a, b are the attributes, while "A" and "B" are the class name's
      b: "B",
    }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* .active {
  color: green;
}
.back {
  background-color: aqua;
}
.color-red {
  color: red;
}
.color-blue {
  color: blue;
} */
.A {
  color: red;
}
.B {
  background-color: black;
}
</style>
