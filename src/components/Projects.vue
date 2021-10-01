<template>
  <section id="projects" class="container">
    <div class="top-section flex">
      <div
        class="section-text"
        data-aos="fade-right"
        data-aos-offset="300"
        data-aos-easing="ease-in-sine"
      >
        <span class="subtitle line-left white">Project</span>
        <h3 class="big-title jamjuree white">
          Our expert trusted consultants help clients
        </h3>
      </div>
      <div
        data-aos="fade-left"
        data-aos-offset="300"
        data-aos-easing="ease-in-sine"
      >
        <button class="btn-slide">
          <i class="fas fa-long-arrow-alt-left"></i>
        </button>
        <button class="btn-slide">
          <i class="fas fa-long-arrow-alt-right"></i>
        </button>
      </div>
    </div>
    <div
      class="bottom-section"
      data-aos="fade-up"
      data-aos-offset="300"
      data-aos-easing="ease-in-sine"
    >
      <div class="cards montserrat">
        <div class="card" v-for="(project, index) in projects" :key="index">
          <img
            :src="require(`../assets/${project.img}`)"
            :alt="project.title"
          />
          <div class="text-card">
            <div class="text-info">
              <span class="project-title white">{{ project.title }}</span>
              <span class="project-category light">{{ project.category }}</span>
            </div>
            <button class="plus-card btn-slide">
              <i class="fas fa-plus"></i>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { projectsHome } from "../assets/data/Projects";
export default {
  name: "Projects",
  data() {
    return {
      projects: projectsHome,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";
#projects {
  padding: 100px 10px;
  .top-section {
    justify-content: space-between;
    align-items: center;

    .section-text {
      max-width: 50%;
    }
  }
  .bottom-section {
    .cards {
      margin-top: 20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-evenly;
      .card {
        width: calc(100% / 3 - 10px);
        height: 350px;
        margin-bottom: 10px;
        min-width: 250px;
        position: relative;
        display: flex;
        align-items: flex-end;
        transition: 0.4s ease-out;
        box-shadow: 0px 7px 10px rgba(black, 0.5);
        &:hover {
          transform: translateY(20px);
          &:before {
            opacity: 1;
          }
          .text-card {
            opacity: 1;
            transform: translateY(0px);
          }
        }
        &:before {
          content: "";
          position: absolute;
          top: 0;
          left: 0;
          display: block;
          width: 100%;
          height: 100%;
          background: rgba($red, 0.8);
          z-index: 2;
          transition: 0.5s;
          opacity: 0;
        }
        img {
          width: 100%;
          height: 100%;
          object-fit: cover;
          position: absolute;
          top: 0;
          left: 0;
        }
        .text-card {
          position: relative;
          z-index: 3;
          color: white;
          opacity: 0;
          transform: translateY(30px);
          transition: 0.5s;
          display: flex;
          justify-content: space-between;
          width: 100%;
          padding: 15px;
          align-items: center;
          .text-info {
            display: flex;
            flex-direction: column;
          }

          .project-title {
            margin: 0px;
            font-size: $fs-h3;
            font-weight: $bold;
          }
          .project-category {
            letter-spacing: 1px;
            font-size: 15px;
            margin-top: 8px;
          }
          button {
            padding: 0.6rem;
            outline: none;
            border: none;
            background: $dark-blue;
            color: $white;
            font-weight: bold;
            cursor: pointer;
            transition: 0.4s ease;
            opacity: 0.9;
            &:hover {
              background-color: $dark-secondary;
              opacity: 1;
            }
          }
          &:hover {
            color: white;
          }
        }
      }
    }
  }
}
</style>