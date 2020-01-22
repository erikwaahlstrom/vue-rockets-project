<template>
  <section>
    <rocket
      v-for="rocket in rockets"
      :rocket="rocket"
      :key="rocket.name"
    ></rocket>
  </section>
</template>

<script>
import { mapGetters } from "vuex";
import Rocket from "./Rocket.vue";

export default {
  props: ["rockets"],
  computed: mapGetters({ rockets: "rockets" }),
  components: {
    Rocket
  }
};
</script>
