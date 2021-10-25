<template>
  <div class="chain">
    <h2>Cosmos Hub</h2>
    <button @click="addChain()">Add to Keplr</button>
  </div>
</template>

<script>
export default {
  name: "AddChain",
  methods: {
    addChain() {
      //example chain for testing: 
     window.keplr.experimentalSuggestChain({
        chainId: "mychain-1",
        chainName: "my new chain",
        rpc: "http://123.456.789.012:26657",
        rest: "http://123.456.789.012:1317",
        bip44: {
          coinType: 118,
        },
        bech32Config: {
          bech32PrefixAccAddr: "cosmos",
          bech32PrefixAccPub: "cosmos" + "pub",
          bech32PrefixValAddr: "cosmos" + "valoper",
          bech32PrefixValPub: "cosmos" + "valoperpub",
          bech32PrefixConsAddr: "cosmos" + "valcons",
          bech32PrefixConsPub: "cosmos" + "valconspub",
        },
        currencies: [
          {
            coinDenom: "ATOM",
            coinMinimalDenom: "uatom",
            coinDecimals: 6,
            coinGeckoId: "cosmos",
          },
        ],
        feeCurrencies: [
          {
            coinDenom: "ATOM",
            coinMinimalDenom: "uatom",
            coinDecimals: 6,
            coinGeckoId: "cosmos",
          },
        ],
        stakeCurrency: {
          coinDenom: "ATOM",
          coinMinimalDenom: "uatom",
          coinDecimals: 6,
          coinGeckoId: "cosmos",
        },
        coinType: 118,
        gasPriceStep: {
          low: 0.01,
          average: 0.025,
          high: 0.03,
        },
      });
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