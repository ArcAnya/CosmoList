<template>
  <div class="chain">
    <!-- TO DO ADD info based on chainData and checking it first -->
    <h2>Cosmos Hub</h2>
    <button @click="addChain()">Add to Keplr</button>
  </div>
</template>

<script>
import chainData from "../../data/MyChain-1.json";

export default {
  name: "AddChain",
  methods: {
    async addChain() {
      if (window.keplr) {
        // TO DO: check that has certain info (chainId) - necessary for button to work
        window.keplr.experimentalSuggestChain(chainData);
        // return window.keplr;
      } else {
        alert(
          "Install the Keplr Wallet browser extension: https://chrome.google.com/webstore/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap?hl=en"
        );
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  display: flex;
}
h2 {
  display: flex;
}
p {
  display: flex;
}
a {
  color: #42b983;
}
.chain {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 20vh;
  width: 10vw;
  background-color: white;
  border-radius: 10%;
  margin: 1%;
}
.button {
  border-radius: 30%;
}
</style>