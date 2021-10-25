<template>
  <div class="fixed-background"></div>
  <div class="welcome">
    <div class="container">
      <h1>CosmoList</h1>
      <h2>Helping users connect to Cosmos Network Blockchains</h2>
      <p>
        CosmoList is a list of Blockchains from the Cosmos Ecosystem. Users can
        use the information to connect their wallets and Web3 middleware
        providers to the appropriate Chain ID and Network ID to connect to the
        correct chain.
      </p>
      <p>
        Warning: This website uses an experimental feature. For more
        information, read the Keplr docs
        <a href="https://docs.keplr.app/api/suggest-chain.html">here</a>.
      </p>
      <a href="#" target="_blank">Add Network #3</a>
      <a href="https://github.com/ArcAnya/CosmoList" target="_blank"
        >View Source Code</a
      >
    </div>
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
a {
  color: #42b983;
}
.welcome {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  background-color: white;
  width: 30vw;
  height: 90vh;
}
.container {
  display: flex;
  flex-direction: column;
  text-align: left;
  margin: 10%;
}
.fixed-background {
  background-color: white;
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 69vw;
  z-index: -1;
}
</style>
