<template>
  <footer class="container px-10">
    <div class="footer-top flex">
      <div class="foot-logo">
        <img src="../assets/img/logo-w.png" alt="" />
      </div>
      <div class="foot-nav">
        <PrimaryMenu />
      </div>
      <div class="foot-socials">
        <a href="#" class="text-reset white"
          ><i class="fab fa-facebook-f"></i
        ></a>
        <a href="#" class="text-reset white"
          ><i class="fab fa-instagram"></i
        ></a>
        <a href="#" class="text-reset white"
          ><i class="fab fa-linkedin-in"></i
        ></a>
        <a href="#" class="text-reset white"><i class="fab fa-twitter"></i></a>
      </div>
    </div>
    <div class="footer-bottom flex">
      <div class="terms">
        <p><a class="text-reset" href="">Term of Use</a></p>
        <p><a class="text-reset" href="">Privacy Environment Policy</a></p>
      </div>
      <div class="copyright">
        <span class="light"
          >Copyright ©2021 Phlox Consulting. All Rights Reserved.</span
        >
      </div>
    </div>
  </footer>
</template>

<script>
import PrimaryMenu from "./micro-components/PrimaryMenu.vue";

export default {
  components: {
    PrimaryMenu,
  },
  name: "Footer",
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

footer {
  font-family: $montserrat;
  background-color: $dark-blue;
  min-height: 250px;
  margin: 0 auto;

  .footer-top {
    justify-content: space-between;
    flex-wrap: wrap;
    padding: 60px 0;
    border-bottom: 1px solid $grey;
    .foot-logo {
      width: 100px;
      img {
        width: 100%;
      }
    }
    .foot-socials {
      color: $white;
      font-size: 20px;

      i {
        margin-left: 10px;
        transition: 0.8s;
        &:hover {
          color: $acquamarine;
        }
      }
    }
  }

  .footer-bottom {
    font-size: $fs-small;
    padding: 40px 0;
    justify-content: space-between;
    a {
      color: $txt-opacity;
      &:hover {
        color: $white;
      }
    }
  }
}
</style>