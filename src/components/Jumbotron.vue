<template>
  <section class="section">
    <div class="jumbotron">
      <div class="container">
        <div class="jumbo-text">
          <h4 class="subtitle">Always the best way you need it</h4>
          <h1>The best business consulting</h1>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style lang="scss" scoped>
@import "@/styles/general.scss";

.jumbotron {
  margin-top: -80px;
  height: 95vh;
  background-image: url("../img/hero.jpg");
  background-repeat: no-repeat;
  background-position: top right;
  background-size: 65%;

  .container {
    margin: auto;
    .jumbo-text {
      max-width: 500px;
      position: absolute;
      top: calc(50% + 40px);
      transform: translateY(-50%);

      h4::before {
        content: "";
        display: inline-block;
        width: 35px;
        height: 2px;
        margin-right: 15px;
        background-color: $acquamarine;
      }

      h1 {
        font-size: $fs-h1;
        font-family: $jamjuree;
        color: $white;
        text-transform: uppercase;
      }
    }
  }
}
</style>