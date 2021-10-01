<template>
  <section id="cta">
    <h3 class="big-title white jamjuree">Let's Talk About Work</h3>
    <p class="paragraph white montserrat">
      A wonderful serenity has taken possession Far far away, behind the word
      mountains.
    </p>
    <button>GET STARTED</button>
  </section>
</template>

<script>
export default {
  name: "HeroCTA",
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";
#cta {
  min-height: 450px;
  background-image: url("../assets/img/CTA-foot.jpg");
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  p {
    text-align: center;
    width: 400px;
    margin-bottom: 20px;
  }

  @include button("dark");
}
</style>