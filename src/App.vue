<template>
  <main>
    <px-header :links="links"></px-header>
    <router-view class="container px-5 sm:px-20 py-20  justify-center" />
  </main>
</template>

<script>
import PxHeader from "@/components/PxHeader";

//import PxAssetsTable from './components/PxAssetsTable.vue';
export default {
  name: "App",
 
  components: {
    PxHeader
  },
   data() {
    return {
      links: [
        {
          title: 'BTC',
          to: { name: 'coin-datial', params: { id: 'bitcoin' } }
        },
        {
          title: 'ETH',
          to: { name: 'coin-datial', params: { id: 'ethereum' } }
        },
        {
          title: 'XRP',
          to: { name: 'coin-datial', params: { id: 'xrp' } }
        }
      ]
    }
  }
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
</style>
