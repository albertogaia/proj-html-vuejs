<template>
  <section id="projects" class="container">
    <div class="top-section flex">
      <div class="section-text">
        <span class="subtitle line-left white">Project</span>
        <h3 class="big-title jamjuree white">
          Our expert trusted consultants help clients
        </h3>
      </div>
      <div>
        <button class="btn-slide">
          <i class="fas fa-long-arrow-alt-left"></i>
        </button>
        <button class="btn-slide">
          <i class="fas fa-long-arrow-alt-right"></i>
        </button>
      </div>
    </div>
    <div class="bottom-section">
      <div class="cards montserrat">
        <div class="card">
          <div class="img-card">
            <img src="../assets/img/project-1.jpg" alt="" />
          </div>
          <div class="card-hover">
            <div class="text-card">
              <span class="project-title white">Purinky Products</span>
              <span class="project-category light">Uncategorized</span>
            </div>

            <button class="plus-card btn-slide">
              <i class="fas fa-plus"></i>
            </button>
          </div>
        </div>
        <div class="card">
          <div class="img-card">
            <img src="../assets/img/project-1.jpg" alt="" />
          </div>
          <div class="card-hover">
            <div class="text-card"></div>
            <div class="plus-card"></div>
          </div>
        </div>
        <div class="card">
          <div class="img-card">
            <img src="../assets/img/project-1.jpg" alt="" />
          </div>
          <div class="card-hover">
            <div class="text-card"></div>
            <div class="plus-card"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Projects",
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
        margin-bottom: 10px;
        min-width: 250px;
        position: relative;
        overflow: hidden;

        .img-card {
          width: 100%;
          position: relative;
          overflow: hidden;

          img {
            width: 100%;
            transition: 1s;
          }
          &:hover {
            transition: 1s;

            &::before {
              content: "";
              position: absolute;
              top: 0;
              left: 0;
              height: 100%;
              width: 100%;
              background: rgba(255, 0, 0, 0.454);
              z-index: 9;
            }
          }
        }

        .card-hover {
          display: flex;
          justify-content: space-between;
          align-items: flex-end;
          position: absolute;
          left: 10px;
          right: 0;
          z-index: 99;

          .text-card {
            .project-title {
              font-size: $fs-h3;
              display: block;
              font-weight: 600;
            }
          }
        }
        &:hover {
          img {
            transform: scale(1.1);
          }
          .card-hover {
            animation: show-text 0.8s 0.3s forwards;
            transition: 1s;
          }
        }
        @keyframes show-text {
          from {
            bottom: 0;
          }
          to {
            bottom: 15px;
          }
        }
      }
    }
  }
}
</style>