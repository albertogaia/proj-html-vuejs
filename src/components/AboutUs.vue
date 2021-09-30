<template>
  <section id="about-us">
    <div class="top">
      <div class="img-about">
        <img src="@/assets/img/about.jpg" alt="about us" />
      </div>
      <div class="text-about">
        <h4 class="subtitle">About Us</h4>
        <h2>We make your strategy work</h2>
        <p>
          When, while lovely valley teems with vapour around meand eridian sun
          strikes the upper impenetrable foliage of my trees, and but a thousand
          unknown plants are noticed when I hear the buzz of the little world
          among the stalks,and grow familiar indescribable forms of the insects
          .and flies, then I feel the presence of the Almighty .
        </p>
      </div>
    </div>
    <div class="bottom-cta">
      <BusinessCareCTA />
    </div>
  </section>
</template>

<script>
import BusinessCareCTA from "./micro-components/BusinessCareCTA.vue";
export default {
  name: "AboutUs",
  components: {
    BusinessCareCTA,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/general.scss";
#about-us {
  font-family: $montserrat;
  .top {
    height: 800px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;

    .img-about {
      height: 100%;
      width: 55%;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
      }
    }
    .text-about {
      color: white;
      padding: 5%;
      width: 35%;

      h2 {
        text-transform: uppercase;
        font-size: $fs-h2;
        font-family: $jamjuree;
      }
      p {
        color: $txt-opacity;
        font-weight: $light;
      }
    }
  }
}
</style>