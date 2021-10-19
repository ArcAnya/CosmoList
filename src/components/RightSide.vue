<template>
  <div class="overall-list">
    <div class="header">
      <div>SEARCH</div>
      <div>THEME</div>
      <button @click="getKeplr()">Connect Wallet #1</button>
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
  data() {
    return {};
  },
  methods: {
    async getKeplr() {
      if (window.keplr) {
        return window.keplr;
      } else {
          console.log("No Kelpr!")
      }

      if (document.readyState === "complete") {
        return window.keplr;
      }

      return new Promise((resolve) => {
        const documentStateChange = (event) => {
          if (event.target && event.target.readyState === "complete") {
            resolve(window.keplr);
            document.removeEventListener(
              "readystatechange",
              documentStateChange
            );
          }
        };

        document.addEventListener("readystatechange", documentStateChange);
      });
    },
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
