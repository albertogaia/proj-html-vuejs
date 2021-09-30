<template>
  <ul class="nav-links">
    <li
      v-for="(item, index) in menu"
      :key="index"
      :class="item.active ? 'active' : null"
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
    };
  },
  methods: {},

  created() {},
};
</script>

<style>
</style>