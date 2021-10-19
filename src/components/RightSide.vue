<template>
  <div class="overall-list">
    <div class="header">
      <div>SEARCH</div>
      <div>THEME</div>
      <button>Connect Wallet #1</button>
    </div>
    <br />
    <div class="list">List of Chains (Components) #2</div>
  </div>
</template>

<script>
export default {
  name: "RightSide",
  props: {
    // msg: String
  },
};
</script>

<style scoped>
.overall-list {
  display: flex;
  background-color: lightgray;
  height: 100vh;
  width: 50vw;
  flex-direction: column;
  justify-content: space-around;
}
.header {
  display: flex;
  justify-content: space-around;
}
.list {
  display: flex;
  justify-content: space-around;
}
</style>
