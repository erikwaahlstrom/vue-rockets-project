<template>
  <section>
    <rocket
      v-for="(singleRocket, index) in rockets"
      :singleRocket="singleRocket"
      :key="index"
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
