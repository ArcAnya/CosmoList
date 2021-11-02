<template>
  <div class="overall-container">
    <div class="header">
      <div class="search-wrapper">
        <input type="text" v-model="search" placeholder="Search Blockchain:" />
      </div>
      <div>Theme</div>
      <button @click="connect()">
        <p v-if="!address">Connect Wallet</p>
        <p v-else>Connected {{address}}</p>
      </button>
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
  data() {
    return {
      keplrInfo: null,
      address: null,
    };
  },
  components: {
    AddChain,
  },
  methods: {
    async connect() {
      if (window.keplr) {
        window.keplr.enable("cosmoshub-4");
        this.keplrInfo = await window.keplr.getKey("cosmoshub-4");
        this.address = this.keplrInfo.bech32Address;
        console.log(this.address);
        // TO DO => with catch / error AND change button to "connected" div when connected (or "disconnect" button to lock again )
      } else {
        alert(
          "Install the Keplr Wallet browser extension: https://chrome.google.com/webstore/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap?hl=en"
        );
      }
    },
  },
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
