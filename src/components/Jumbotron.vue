<template>
  <section class="section">
    <div class="jumbotron">
      <div class="container px-10">
        <div class="jumbo-text">
          <span class="subtitle line-left white"
            >Always the best way you need it</span
          >
          <h1>The best business consulting</h1>
          <div class="ctas">
            <button><a href="#about">Read More</a></button>
            <div class="play-button"><i class="fas fa-play"></i></div>
          </div>
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

      @include button("primary");

      h1 {
        font-size: $fs-h1;
        font-family: $jamjuree;
        color: $white;
        text-transform: uppercase;
      }
      .ctas {
        margin-top: 15px;
        display: flex;
        align-items: center;
      }
      .play-button {
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        border: 2px solid $white;
        width: 40px;
        height: 40px;
        margin-left: 25px;
        cursor: pointer;
        transition: 0.5s;

        i {
          font-size: 15px;
          color: $acquamarine;
        }

        &:hover {
          transform: scale(1.1);
          background: $red;
        }
      }
    }
  }
}
</style>