<template>
  <div class="overall-list">
    <div class="header">
      <div>Search</div>
      <div>Theme</div>
      <button @click="getKeplr()">Connect Wallet #1</button>
    </div>
    <br />
    <div class="list">
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

import AddChain from "./AddChain.vue"

export default {
  name: "RightSide",
  components: {
    AddChain
  },
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
        alert(
          "Install the Keplr Wallet browser extension: https://chrome.google.com/webstore/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap?hl=en"
        );
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
  height: 90vh;
  width: 70vw;
  flex-direction: column;
  justify-content: space-around;
}
.header {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.list {
  display: flex;
  /* justify-content: space-around; */
  align-items: center;
  flex-wrap: wrap;
}
button {
  border-radius: 5%;
  padding: 1%;
}
</style>
