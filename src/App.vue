<template>
  <div class="Overall">
    <LeftSide />
    <RightSide />
  </div>
</template>

<script>
import LeftSide from "./components/LeftSide.vue";
import RightSide from "./components/RightSide.vue";

export default {
  name: "App",
  components: {
    LeftSide,
    RightSide,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.Overall {
  display: flex;
  flex-direction: row;
}
</style>
