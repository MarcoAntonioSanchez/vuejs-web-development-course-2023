<template>
  <!--
    RENDERING LIST
    Generating name's list by binding with v-for, using item's id as key
    <div v-for="item in myList" :key="item.id">
      {{ item.name }}
    </div>

    Destructuring the data inside myList, same result as above
    <div v-for="{ name, id } in myList" :key="id">
      {{ name }}
    </div>

    USING CONDITIONAL EXPRESSIONS IN LISTS
    <div v-for="{ name, id, isActive } in myList" :key="id">
      If the attribute is true, HTML tag H1 is shown, otherwise it won't be displayed
      <h1 v-if="isActive" class="header">
        {{ name }}
      </h1>
    </div>
    
    SENDING DATA IN LIST TO FUNCTION
    Using @click to run the myData function, allong with the name attribute passed
    <div @click="myData(name)" v-for="{ name, id, isActive } in myList" :key="id">
      <h1 v-if="isActive" class="header">
        {{ name }}
      </h1>
    </div>
  -->

  <div v-for="(item, index) in myList" :key="index">
    <h1 @click="removeData(index)" class="header">
      {{ item.name }}
    </h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: { // New function to receive "name" on click over the div container
    myData(data) { // name is used to send it, data will receive it
      console.log(data); // Get's printed in console
    },
    removeData(index) {
      this.myList.splice(index, 1) // Using splice method to separate attribute index with position 1
    }
  },
  data() {
    return {
      myList: [
        {
          id: 1,
          name: "John",
          isActive: true, // Boolean comprobation added to the objects attributes
        },
        {
          id: 2,
          name: "Jack",
          isActive: false,
        },
        {
          id: 3,
          name: "Raven",
          isActive: true,
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
.header {
  border: 1px solid orangered;
  background-color: orangered;
  color: black;
  padding: 1rem;
}
</style>
