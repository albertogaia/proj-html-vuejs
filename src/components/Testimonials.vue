<template>
  <section id="testimonials">
    <div class="top-section flex container px-10">
      <div
        class="section-text"
        data-aos="fade-left"
        data-aos-offset="50"
        data-aos-easing="ease-in-sine"
      >
        <span class="subtitle line-right white">Testimonial</span>
        <h3 class="big-title jamjuree white">
          What's the customer say about our work
        </h3>
      </div>
    </div>
    <div
      class="bottom-section container-aside"
      data-aos="fade-left"
      data-aos-offset="50"
      data-aos-easing="ease-in-sine"
    >
      <template>
        <div class="container-inside">
          <div
            class="testimonial montserrat"
            v-for="(testimonial, index) in testimonials"
            :key="index"
            :id="index"
          >
            <img :src="require(`../assets/${testimonial.img}`)" alt="" />
            <div class="single-testimonial p-50">
              <p class="paragraph">
                {{ testimonial.text }}
              </p>
              <span class="jamjuree testimonial-name">{{
                testimonial.name
              }}</span>
              <span class="testimonia-industry">{{
                testimonial.industry
              }}</span>
            </div>
          </div>
        </div>
      </template>
    </div>
  </section>
</template>

<script>
import { testimonials } from "../assets/data/Testimonials";
export default {
  name: "Testimonials",
  data() {
    return {
      testimonials: testimonials,
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";
#testimonials {
  position: relative;

  .top-section {
    justify-content: flex-end;
    .section-text {
      max-width: 450px;
      .subtitle {
        width: 100%;
        text-align: end;
      }
    }
  }
  .bottom-section {
    margin: 0 0px 0 auto;
    background-color: $white;
    .container-inside {
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-start;
      max-width: 1440px;
    }
    .testimonial {
      display: flex;
      flex-wrap: wrap;
      position: relative;
      overflow: hidden;
      width: calc(100% / 3);
      min-width: 300px;
      img {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        transition: 1s ease-in-out;
        object-fit: cover;
        object-position: center;
        width: 100%;
        height: 100%;
        z-index: 1;
        opacity: 0;
      }
      &:hover img {
        opacity: 1;
      }
      .single-testimonial {
        width: 100%;
        transition: 0.5s;
        z-index: 3;
        &:hover {
          color: $white;
          text-shadow: 3px 3px 10px $dark-blue;
        }
        .testimonial-name {
          display: block;
          font-weight: $bold;
          font-size: $fs-h4;
          margin: 15px 0 5px;
        }
        .testimonial-industry {
          font-size: $fs-p;
        }
      }
    }
  }
}
</style>