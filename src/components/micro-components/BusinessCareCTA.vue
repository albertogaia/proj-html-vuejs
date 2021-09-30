<template>
  <div class="cta">
    <h4 class="jamjuree title-section px-10">
      We help to deliver the business care
    </h4>
    <p>
      When, while lovely valley teems with vapour around meand meridian sun
      strikes the upper impenetrable foliage of my trees, and but a thousand
      unknown
    </p>
    <button>Get started</button>
  </div>
</template>

<script>
export default {
  name: "BusinessCareCTA",
};
</script>

<style lang="scss" scoped>
@import "@/styles/general.scss";

.cta {
  width: 90%;
  height: 300px;
  position: relative;
  background-color: $acquamarine;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  h4 {
    width: 250px;
    font-size: $fs-h3;
    text-transform: uppercase;
    font-family: $jamjuree;
  }
  p {
    width: 500px;
    font-weight: $light;
  }
  @include button("red");
  button {
    position: absolute;
    right: 0;
    bottom: 0;
  }
}
</style>