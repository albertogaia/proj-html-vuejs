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
import { primaryMenu } from "@/assets/data/Links.js";
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

<style>
</style>