<template>
  <div id="app">
    <div id="scroller"></div>
    <Header />
    <Jumbotron />
    <Services />
    <About />
    <Projects />
    <Testimonials />
    <Blog />
    <HeroCTA />
    <Footer />

    <div class="fixed-bottom" id="myBtn">
      <a href="#"
        ><div class="up-to-page">
          <i class="fas fa-arrow-up"></i></div
      ></a>
      <button class="chat" @click="getChatBox">
        <i class="far" :class="iconChat"></i>
      </button>
    </div>
    <transition name="chat">
      <Chatbox v-show="visible" />
    </transition>
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
import Chatbox from "./components/micro-components/Chatbox.vue";
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
    Chatbox,
  },
  data() {
    return {
      visible: false,
      iconChat: "",
    };
  },
  methods: {
    scrollFunction() {
      let mybutton = document.getElementById("myBtn");
      if (
        document.body.scrollTop > 400 ||
        document.documentElement.scrollTop > 400
      ) {
        mybutton.style.display = "block";
      } else {
        mybutton.style.display = "none";
      }
    },

    getChatBox() {
      if (this.visible == true) {
        this.visible = false;
        this.iconChat = "far fa-comment";
      } else {
        this.visible = true;
        this.iconChat = "fas fa-times";
      }
    },
  },
  mounted() {
    window.addEventListener("scroll", this.scrollFunction);
  },
  created() {
    this.iconChat = "fa-comment";
  },
};
</script>

<style lang="scss">
@import "styles/general.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";
html {
  scroll-behavior: smooth;
}
.chat-leave-from {
  opacity: 1;
  transform: translateX(0);
}
.chat-leave-to {
  opacity: 0;
  transform: translateX(200px);
}
.chat-leave-active {
  transition: all 0.3s ease-out;
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
  overflow: hidden;

  #myBtn {
    transition: 2s;
    .up-to-page {
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: $white;
      position: fixed;
      bottom: 20px;
      right: 100px;
      width: 40px;
      height: 40px;
      border-radius: 50%;
      transition: 0.2s;
      box-shadow: 3px 3px 20px rgba($dark-blue, 0.4);
      &:hover {
        transform: scale(1.1);
      }
    }

    .chat {
      display: flex;
      position: fixed;
      justify-content: center;
      align-items: center;
      font-size: $fs-h3;
      bottom: 20px;
      right: 20px;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background-color: $blue;
      color: $white;
      border: none;
      cursor: pointer;
      transition: 0.5s;
      box-shadow: 3px 3px 20px rgba($dark-blue, 0.4);

      &:hover {
        transform: scale(1.1);
      }
    }
  }
}
</style>
