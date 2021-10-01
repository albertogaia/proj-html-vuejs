<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Services />
    <About />
    <Projects />
    <Testimonials />
    <Blog />
    <HeroCTA />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Services from "./components/Services.vue";
import About from "./components/AboutUs.vue";
import Projects from "./components/Projects.vue";
import Testimonials from "./components/Testimonials.vue";
import Blog from "./components/Blog.vue";
import HeroCTA from "./components/HeroCTA.vue";
import Footer from "./components/Footer.vue";
import AOS from "aos";
import "aos/dist/aos.css";
AOS.init();

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Services,
    About,
    Projects,
    Testimonials,
    Blog,
    HeroCTA,
    Footer,
  },
};
</script>

<style lang="scss">
@import "styles/general.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
html {
  scroll-behavior: smooth;
}
::-webkit-scrollbar {
  width: 1.2em;
}

::-webkit-scrollbar-track {
  background-color: $dark-secondary;
}
::-webkit-scrollbar-thumb {
  border-radius: 20px;
  background-color: $dark-blue;

  &:hover {
    background-color: $acquamarine;
  }
}

@supports (scrollbar-color: $dark-secondary $dark-blue) {
  * {
    scrollbar-color: $dark-secondary $dark-blue;
    scrollbar-width: thin;
  }
}
#app {
  background-color: $dark-blue;
}
</style>
