<template>
  <div>
    <h3>{{ name }}</h3>
    <h3>{{ obj.name }}</h3>
    <button @click="test">Click</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    test() {
      console.log(this.name, this.bool);
    }
  },
  // In Vuej.js the data object is the place where the data used in the Vue component is stored
  // Represents the data model of the component
  // Is the source of the variables and states used in the Vue component
  // Its data can be use in the component's template
  // And gets re render when the component changes
  data() {
    return {
      name: "Elton",
      obj: {
        name: "Marry"
      },
      arr: [],
      bool: true,
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
