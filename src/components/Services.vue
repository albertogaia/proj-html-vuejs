<template>
  <section id="services" class="px-100">
    <div class="container-small">
      <h4 class="jamjuree title-section px-10">Our consultants can help you</h4>
      <div class="cards px-10">
        <div class="card">
          <div class="icon-card">
            <i class="far fa-chart-bar"></i>
          </div>
          <div class="text-card">
            <h4>Statistical Consulting</h4>
            <div class="line"></div>
            <p>
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
            </p>
          </div>
        </div>
        <div class="card">
          <div class="icon-card">
            <i class="fas fa-bullhorn"></i>
          </div>
          <div class="text-card">
            <h4>DIGITAL CONSULTING</h4>
            <p>
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
            </p>
          </div>
        </div>
        <div class="card">
          <div class="icon-card">
            <i class="fas fa-wallet"></i>
          </div>
          <div class="text-card">
            <h4>BANKING CONSULTING</h4>
            <p>
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
            </p>
          </div>
        </div>
        <div class="card">
          <div class="icon-card">
            <i class="fas fa-bullseye"></i>
          </div>
          <div class="text-card">
            <h4>ENTERPRISE CONSULTING</h4>
            <p>
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Services",
};
</script>

<style lang="scss" scoped>
@import "@/styles/general.scss";

#services {
  background-color: white;
  position: relative;
  .title-section {
    // position: relative;
    text-transform: uppercase;
    font-size: $fs-title;
    margin-bottom: 100px;

    &::after {
      display: inline-block;
      content: "";
      position: absolute;
      top: 110px;
      transform: translateY(-50%);
      right: 0;
      width: 60%;
      overflow: hidden;
      height: 3px;
      background-color: $acquamarine;
    }
  }

  .cards {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    .card {
      font-family: $montserrat;
      font-weight: 300;
      display: flex;
      flex-wrap: wrap;
      margin-bottom: 80px;
      .icon-card {
        width: 40px;
        height: 40px;
        background-color: $red;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;

        i {
          color: white;
          font-size: 24px;
        }
      }
      .text-card {
        width: 400px;
        margin-left: 20px;
        p {
          font-size: $fs-p;
        }
        h4 {
          font-size: $fs-title;
          text-transform: uppercase;
          font-family: $jamjuree;
          margin-bottom: 15px;
        }
      }
    }
  }
}
</style>