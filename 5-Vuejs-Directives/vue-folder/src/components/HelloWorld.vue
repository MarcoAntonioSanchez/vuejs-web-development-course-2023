<template>
<!--
  V-HTML
  This one is wrapped by b tags
  <div>{{ myContent }}</div>
  This one don't
  <div v-html="myContent"></div>
  <div>
    V-TEXT
    This one shows the "Hello, How are you. string"
    <h1 v-text="myText"></h1>
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
      myText: "Hello, How are you.",
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
