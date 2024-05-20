<template>
  <!--
    Generating name's list by binding with v-for, using item's id as key
    <div v-for="item in myList" :key="item.id">
      {{ item.name }}
    </div>
  -->

  <!--
    Destructuring the data inside myList, same result as above
    <div v-for="{ name, id } in myList" :key="id">
      {{ name }}
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
      myList: [
        {
          id: 1,
          name: "John"
        },
        {
          id: 2,
          name: "Jack"
        },
        {
          id: 3,
          name: "Raven"
        }
      ]
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
