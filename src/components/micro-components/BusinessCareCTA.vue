<template>
  <div class="cta">
    <h3 class="jamjuree title px-10">We help to deliver the business care</h3>
    <p class="paragraph">
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
@import "../../styles/general.scss";

.cta {
  width: 90%;
  height: 300px;
  position: relative;
  background-color: $acquamarine;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  h3 {
    width: 250px;
  }
  p {
    width: 500px;
  }
  @include button("red");
  button {
    position: absolute;
    right: 0;
    bottom: 0;
  }
}
</style>