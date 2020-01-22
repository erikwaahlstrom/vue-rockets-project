<template>
  <section>
    <h2>{{ rocket.name }}</h2>
    <p>{{ rocket.country }}</p>
    <p>{{ rocket.description }}</p>
    <img class="rocket-images" :src="rocket.image" />
    <button @click="removeRocket(rocket)" type="button">Delete</button>
  </section>
</template>

<script>
import { mapMutations } from "vuex";

export default {
  props: ["rocket"],
  methods: mapMutations(["removeRocket"])
};
</script>

<style>
.rocket-images {
  width: 100px;
}
</style>
