<template>
  <section>
    <rocket
      v-for="singleRocket in rockets"
      :singleRocket="singleRocket"
      :key="singleRocket.id"
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
