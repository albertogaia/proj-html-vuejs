<template>
  <ul class="nav-links">
    <li
      v-for="(item, index) in menu"
      :key="index"
      :class="item == currentLink ? 'active' : null"
      @click="getCurrentLink(index)"
    >
      <a :href="item.url">{{ item.text }}</a>
    </li>
  </ul>
</template>

<script>
import { primaryMenu } from "../../assets/data/Links.js";
export default {
  name: "PrimaryMenu",
  data() {
    return {
      menu: primaryMenu,
      currentLink: "",
    };
  },
  methods: {
    getCurrentLink(i) {
      let tmpLink = this.menu[i];
      this.currentLink = tmpLink;
    },
  },

  created() {
    this.currentLink = this.menu[0];
  },
};
</script>

<style lang="scss" scoped>
@import "../../styles/general.scss";
header {
  .nav-links {
    font-family: $montserrat;
    list-style: none;
    text-transform: uppercase;
    li {
      display: inline-block;
      text-align: center;
      min-width: max-content;
      margin: 0 10px;
      font-weight: 300;
      opacity: 0.7;
      &:hover {
        opacity: 1;
      }
    }
    .active {
      -webkit-box-shadow: inset 0px 3px 0px $white;
      -moz-box-shadow: inset 0px 3px 0px $white;
      box-shadow: inset 0px 3px 0px 0px $white;
      opacity: 1;
      font-weight: 500;
    }
    a {
      text-decoration: none;
      color: $white;
    }
  }
}
footer {
  .nav-links {
    font-family: $montserrat;
    list-style: none;
    text-transform: uppercase;
    li {
      display: inline-block;
      text-align: center;
      min-width: max-content;
      margin: 0 10px;
      font-weight: 300;
      opacity: 0.7;
      &:hover {
        opacity: 1;
      }
    }

    a {
      text-decoration: none;
      color: $white;
    }
  }
}
</style>