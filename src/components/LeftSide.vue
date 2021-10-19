<template>
  <div class="welcome">
    <h1>CosmoList</h1>
    <h2>Helping users connect to Cosmos Network Blockchains</h2>
    <p>
      CosmoList is a list of Blockchains from the Cosmos Ecosystem. Users can
      use the information to connect their wallets and Web3 middleware providers
      to the appropriate Chain ID and Network ID to connect to the correct
      chain.
    </p>
    <a href="#" target="_blank">Add Network #3</a>
    <a href="https://github.com/ArcAnya/CosmoList" target="_blank">View Source Code</a>
  </div>
</template>

<script>
export default {
  name: "LeftSide",
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
.welcome {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 100vh;
  width: 50vw;
}
</style>
