<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Jumbotron from "./components/Jumbotron.vue";

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/styles/general.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

#app {
  background-color: $dark-blue;
}
</style>
