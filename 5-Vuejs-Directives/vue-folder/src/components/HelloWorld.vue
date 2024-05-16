<template>
  <!-- This one is wrapped by b tags -->
  <div>{{ myContent }}</div>
  <!-- This one don't -->
  <div v-html="myContent"></div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {},
  data() {
    return {
      myContent: "<b style='color:red;'>Hello my content</b>"
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
