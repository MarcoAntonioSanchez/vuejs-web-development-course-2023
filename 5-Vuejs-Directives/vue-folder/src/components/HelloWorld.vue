<template>
<!--
    V-HTML
  This one is wrapped by b tags
  <div>{{ myContent }}</div>
  This one don't
  <div v-html="myContent"></div>
  
  V-TEXT
  This one shows the "Hello, How are you. string"
  <div>
  <h1 v-text="myText"></h1>
  </div>

  V-ONCE
  <div>
    This one is only "loaded" once, so the button that trigger myName won't work here
    <h1 v-once>{{ myName }}</h1>
    But in this one, will work and change the "Jane" string for "New Name" string
    <h1>{{ myName }}</h1>
    <button @click="myName='New Name'">Click</button>
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
      myName: "Jane",
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
