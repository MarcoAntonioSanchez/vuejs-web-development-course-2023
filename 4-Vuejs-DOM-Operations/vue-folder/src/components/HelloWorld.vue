<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 :id="myH2">Hello</h2>
    <div v-bind:id="myId">Hello my div: {{ myId }}</div>
    <img v-bind:src="mySrc" alt="">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      myId: "divId",
      myH2: "myH2",
      mySrc: "https://img.freepik.com/premium-vector/raven-stylized-illustration-design-crow-logo-intricate-details_801948-7.jpg",
    };
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#divId {
  background-color: red;
}
#myH2 {
  background-color: cadetblue;
}
</style>
