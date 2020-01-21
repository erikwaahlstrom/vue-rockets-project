<template>
  <section>
    <nav-bar></nav-bar>
    <rockets></rockets>
  </section>
</template>

<script>
import Rockets from "./views/Rockets.vue";
import NavBar from "./components/NavBar.vue";

export default {
  name: "app",
  components: {
    Rockets,
    NavBar
  }
};
</script>

<style>
</style>
