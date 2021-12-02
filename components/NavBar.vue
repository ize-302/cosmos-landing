<!-- Please remove this file from your project -->
<template>
  <nav class="container">
    <Logo />
    <ul class="menu">
      <li v-for="item in menus" :key="item.name">
        <a :href="'#' + item.name">{{ item.name }}</a>
      </li>
    </ul>
    <button class="call-to-action">Start now</button>
    <button
      class="hamburger"
      :class="{ active: hamburgerIsActive }"
      @click="hamburgerIsActive = !hamburgerIsActive"
    >
      <span />
      <span />
    </button>
    <ul class="menu__mobile" v-if="hamburgerIsActive">
      <li v-for="item in menus" :key="item.name">
        <a :href="'#' + item.name">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts">
import Logo from "./Logo.vue";
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      hamburgerIsActive: false,
      menus: [
        {
          name: "Learn",
        },
        {
          name: "Build",
        },
        {
          name: "Explore",
        },
      ],
    };
  },
  components: {
    Logo,
  },
});
</script>
