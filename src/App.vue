<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Services />
    <About />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Services from "./components/Services.vue";
import About from "./components/AboutUs.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Services,
    About,
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
