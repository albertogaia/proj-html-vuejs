<template>
  <section id="blog" class="container">
    <div class="top-section flex">
      <div class="section-text">
        <span class="subtitle line-left white">Blog</span>
        <h3 class="big-title jamjuree white">The recent News you must read</h3>
      </div>
      <div>
        <button class="view-all">View All</button>
      </div>
    </div>
    <div class="bottom-section">
      <div class="card">
        <img src="../assets/img/blog-1.jpg" alt="" class="img-card" />
        <div class="info-card montserrat">
          <a href="" class="text-reset dark-blue">
            <p class="meta-data">
              July 4, 2019 <span class="author"> by paul</span>
            </p>
            <h3 class="title-blog">
              Canadian consulting firm acquired by Giant UK
            </h3>
            <p class="paragraph">
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
              ...
            </p>
          </a>
        </div>
      </div>
      <div class="card">
        <img src="../assets/img/blog-1.jpg" alt="" class="img-card" />
        <div class="info-card montserrat">
          <a href="" class="text-reset dark-blue">
            <p class="meta-data">
              July 4, 2019 <span class="author"> by paul</span>
            </p>
            <h3 class="title-blog">
              Canadian consulting firm acquired by Giant UK
            </h3>
            <p class="paragraph">
              When, while lovely valley teems with vapour around meand eridian
              sun strikes the upper impenetrable foliage of my trees, and but a
              ...
            </p>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Blog",
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

#blog {
  padding-top: 100px;
  .top-section {
    justify-content: space-between;
    align-items: center;
    @include button("primary");
  }
  .bottom-section {
    display: flex;
    justify-content: space-around;
    .card {
      width: calc(100% / 2 - 50px);
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      overflow: hidden;

      &:hover .info-card {
        transform: translateY(-120px);
        background-color: $acquamarine;
      }
      &:hover img {
        transform: scale(1.1);
        filter: blur(2px);
      }
      img {
        transition: 0.8s;
        width: 100%;
      }
      .info-card {
        transition: 0.8s;
        transform: translateY(-150px);
        width: 70%;
        background-color: $white;
        padding: 5%;

        .meta-data {
          color: $red;
          .author {
            display: inline-block;
            margin: 0 15px;
          }
        }
        .title-blog {
          margin: 10px 0;
          font-weight: $bold;
        }
      }
    }
  }
}
</style>