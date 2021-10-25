<template>
  <div class="chain">
    <h2>Cosmos Hub</h2>
    <button @click="addChain()">Add to Keplr</button>
  </div>
</template>

<script>
import chainData from "../../data/TestChain.json";

export default {
  name: "AddChain",
  methods: {
    addChain() {
  
      window.keplr.experimentalSuggestChain( chainData
        //check that has certain info (chainId) - necessary for button to work
      );
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