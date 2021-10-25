<template>
  <div class="overall-container">
    <div class="header">
      <div class="search-wrapper">
        <input type="text" v-model="search" placeholder="Search Blockchain:" />
      </div>
      <div>Theme</div>
    </div>
    <br />
    <div class="list">
      <!-- TO DO => search for a Blockchain in JSON files => progressive search! -->
      <!-- TO DO => logic to get data/props from the JSON files to show the info on components-->

      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
      <AddChain />
    </div>
  </div>
</template>

<script>
import AddChain from "./AddChain.vue";

export default {
  name: "RightSide",
  components: {
    AddChain,
  },
  methods: {},
};
</script>

<style scoped>
.overall-container {
  display: flex;
  height: 90vh;
  width: 70vw;
  flex-direction: column;
  justify-content: space-around;
}
.header {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 1%;
}
.list {
  display: flex;
  /* justify-content: space-around; */
  align-items: center;
  flex-wrap: wrap;
  overflow-y: scroll;
}
button {
  border-radius: 5%;
  padding: 1%;
}
</style>
