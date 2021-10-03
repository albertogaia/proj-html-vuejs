<template>
  <section
    id="blog"
    class="container"
    data-aos="fade-up"
    data-aos-offset="50"
    data-aos-easing="ease-in-sine"
  >
    <div class="top-section flex px-10">
      <div class="section-text">
        <span class="subtitle line-left white">Blog</span>
        <h3 class="big-title jamjuree white">The recent News you must read</h3>
      </div>
      <div>
        <button class="view-all" id="view-all-posts" @click="getMore">
          View More
        </button>
      </div>
    </div>
    <div class="bottom-section">
      <transition-group name="fade" class="bottom-section">
        <div class="card" v-for="(post, index) in posts" :key="index">
          <img
            :src="require(`../assets/${post.img}`)"
            alt=""
            class="img-card"
          />
          <div class="info-card montserrat">
            <a :href="post.url" class="text-reset dark-blue">
              <p class="meta-data">
                {{ post.data }} <span class="author"> {{ post.author }}</span>
              </p>
              <h3 class="title-blog">
                {{ post.title }}
              </h3>
              <p class="paragraph">
                {{ post.summary }}
              </p>
            </a>
          </div>
        </div>
      </transition-group>
    </div>
  </section>
</template>

<script>
import { blogPosts } from "../assets/data/BlogPosts";
export default {
  name: "Blog",
  data() {
    return {
      posts: blogPosts.slice(0, 2),
      more: false,
    };
  },
  methods: {
    getMore() {
      if (this.posts.length == 2) {
        this.posts = blogPosts;
        document.getElementById("view-all-posts").innerText = "View Less";
      } else {
        this.posts = blogPosts.slice(0, 2);
        document.getElementById("view-all-posts").innerText = "View More";
      }
    },
  },
  created() {},
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
    flex-wrap: wrap;

    .fade-enter-active,
    .fade-leave-active {
      transition: opacity 1s;
    }
    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
      opacity: 0;
    }
    .card {
      width: calc(100% / 2 - 50px);
      min-width: 400px;
      position: relative;
      display: flex;
      flex-wrap: wrap;
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