<template>
  <section id="testimonials">
    <div class="top-section flex container px-10">
      <div class="section-text">
        <span class="subtitle line-right white">Testimonial</span>
        <h3 class="big-title jamjuree white">
          What's the customer say about our work
        </h3>
      </div>
    </div>
    <div class="bottom-section container-aside">
      <template>
        <div class="testimonial montserrat">
          <div class="single-testimonial p-50">
            <p class="paragraph">
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
              thousand unknown plants are noticed by when I hear the buzz of the
              little .
            </p>
            <span class="jamjuree testimonial-name">Vera Duncan</span>
            <span class="testimonia-industry">Amazon Inc.</span>
          </div>
        </div>
        <div class="testimonial montserrat">
          <div class="single-testimonial p-50">
            <p class="paragraph">
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
              thousand unknown plants are noticed by when I hear the buzz of the
              little .
            </p>
            <span class="jamjuree testimonial-name">Vera Duncan</span>
            <span class="testimonia-industry">Amazon Inc.</span>
          </div>
        </div>
        <div class="testimonial montserrat">
          <div class="single-testimonial p-50">
            <p class="paragraph">
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
              thousand unknown plants are noticed by when I hear the buzz of the
              little .
            </p>
            <span class="jamjuree testimonial-name">Vera Duncan</span>
            <span class="testimonia-industry">Amazon Inc.</span>
          </div>
        </div>
      </template>
    </div>
  </section>
</template>

<script>
export default {
  name: "Testimonials",
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
    margin: 0 0 0 auto;
    background-color: $white;
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;

    .testimonial {
      display: flex;
      flex-wrap: wrap;
      .single-testimonial {
        max-width: 450px;
        transition: 0.8s;
        &:hover {
          background-image: url("../assets/img/testimonial-1.jpg");
          background-position: center;
          background-size: cover;
          color: $white;
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