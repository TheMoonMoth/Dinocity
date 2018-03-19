<template>
  <div id="app">
    <Header></Header>
    <router-view v-bind:listings='listings' />
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer
  },
  data() {
    listings: [];
  },
  mounted() {
    const API_URL = "../../static/listings.json";
    fetch(API_URL)
      .then(res => res.json())
      .then(json => {
        console.log("Api response", json);
        return json;
      })
      .then(json => {(this.listings = json)})
      .catch(console.error("something went wrong during our API request"));
  }
};
</script>

<style>

</style>
