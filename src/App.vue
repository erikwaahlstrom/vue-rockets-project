<template>
  <section>
    <nav-bar></nav-bar>
    <rockets></rockets>
  </section>
</template>

<script>
import Rockets from "./views/Rockets.vue";

export default {
  name: "app",
  components: {
    Rockets,
  }
};
</script>

<style>
</style>
