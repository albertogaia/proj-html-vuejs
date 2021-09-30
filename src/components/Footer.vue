<template>
  <footer class="container">
    <div class="footer-top flex">
      <div class="foot-logo">
        <img src="@/img/logo-w.png" alt="" />
      </div>
      <div class="foot-nav">
        <PrimaryMenu />
      </div>
      <div class="foot-socials">
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-instagram"></i>
        <i class="fab fa-linkedin-in"></i>
        <i class="fab fa-twitter"></i>
      </div>
    </div>
    <div class="footer-bottom flex">
      <div class="terms">
        <p><a class="text-reset" href="">Term of Use</a></p>
        <p><a class="text-reset" href="">Privacy Environment Policy</a></p>
      </div>
      <div class="copyright">
        <p>
          <a class="text-reset" href=""
            >Copyright ©2021 Phlox Consulting. All Rights Reserved.</a
          >
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import PrimaryMenu from "./PrimaryMenu.vue";

export default {
  components: {
    PrimaryMenu,
  },
  name: "Footer",
};
</script>

<style lang="scss" scoped>
@import "@/styles/general.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

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
      }
    }
  }

  .footer-bottom {
    padding: 40px 0;
    justify-content: space-between;
    a {
      color: $txt-opacity;
      font-size: $fs-p;
    }
  }
}
</style>