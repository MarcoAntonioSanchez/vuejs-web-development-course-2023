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

  <!--
    Bindigng example, using an array for multiple classes
    <div>
      <h1 :class="[a, b]">Hello</h1>
    </div>
  -->

  <!-- 
    Final binding example for style (CSS) class name's
    <div>
      In-line example #1:
      <h1 :style="{color:color, fontWeight:fontWeight}">Hello</h1>
      In-line shorter example #2:
      <h1 :style="{color, fontWeight}">Hello</h1>
      In-line super short example #3:
      <h3 :style="styleObj">Hello</h3>
    </div>
  -->
  <div></div>
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
      color: "purple",
      fontWeight: "800",
      styleObj: {
        color: "red",
        backgroundColor: "blue"
      },
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
}
.A {
  color: red;
}
.B {
  background-color: black;
} */

</style>
