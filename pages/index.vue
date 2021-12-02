<template>
  <div>
    <nav-bar />
    <hero />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import NavBar from "~/components/NavBar.vue";
import Hero from "~/components/Hero.vue";

export default Vue.extend({
  components: { NavBar, Hero },
});
</script>
