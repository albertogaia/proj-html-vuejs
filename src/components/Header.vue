<template>
  <header class="container flex">
    <div class="logo">
      <img src="@/img/logo.png" alt="logo" />
    </div>
    <div class="navmenu">
      <ul class="nav-links">
        <li class="active"><a href="">Home</a></li>
        <li><a href="">About</a></li>
        <li><a href="">Projects</a></li>
        <li><a href="">Services</a></li>
        <li><a href="">Blog</a></li>
        <li><a href="">Contact</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
@import "@/styles/general.scss";

header {
  height: 80px;
  line-height: 80px;
  justify-content: space-between;
  margin: 0 auto;

  .logo {
    width: 100px;
    img {
      width: 100%;
    }
  }

  .nav-links {
    font-family: $montserrat;
    list-style: none;

    li {
      display: inline-block;
      text-align: center;
      min-width: max-content;
      margin: 0 10px;
      font-weight: 300;
      opacity: 0.5;

      &:hover {
        opacity: 1;
      }
    }
    .active {
      border-top: 3px solid $white;
      opacity: 1;
      font-weight: 500;
    }

    a {
      text-decoration: none;
      color: $white;
    }
  }
}
</style>