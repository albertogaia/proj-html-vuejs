<template>
  <section id="services" class="px-100">
    <div class="container-small">
      <h3 class="jamjuree title px-10">Our consultants can help you</h3>
      <div class="cards px-10">
        <div class="card">
          <div class="icon-card">
            <i class="far fa-chart-bar"></i>
          </div>
          <div class="text-card">
            <h4 class="title">Statistical Consulting</h4>
            <div class="line"></div>
            <p class="paragraph">
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
            <h4 class="title">DIGITAL CONSULTING</h4>
            <p class="paragraph">
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
            <h4 class="title">BANKING CONSULTING</h4>
            <p class="paragraph">
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
            <h4 class="title">ENTERPRISE CONSULTING</h4>
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
@import "../styles/general.scss";

#services {
  background-color: white;
  position: relative;
  h3.title {
    margin-bottom: 100px;

    &::after {
      display: inline-block;
      content: "";
      position: absolute;
      top: 130px;
      transform: translateY(-50%);
      right: 0;
      width: 55%;
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
      }
    }
  }
}
</style>