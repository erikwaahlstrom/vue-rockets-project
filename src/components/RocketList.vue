<template>
  <section>
    <rocket
      v-for="rocket in rockets"
      :rocket="rocket"
      :key="rocket.id"
      :removeRocket="removeRocket"
    ></rocket>
  </section>
</template>

<script>
import Rocket from "./Rocket.vue";
export default {
  props: ["rockets", "removeRocket"],
  components: {
    Rocket
  }
};
</script>
