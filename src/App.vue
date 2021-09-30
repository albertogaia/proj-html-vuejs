<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Services />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Services from "./components/Services.vue";

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Services,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/styles/general.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
html {
  scroll-behavior: smooth;
}
#app {
  background-color: $dark-blue;
}
</style>
