<template>
  <section>
    <h2>{{singleRocket.name}}</h2>
    <p>{{singleRocket.country}}</p>
    <p>{{singleRocket.description}}</p>
    <img class="rocket-images" :src="singleRocket.image" />
    <button @click="removeRocket(index)" type="button">Delete</button>
  </section>
</template>

<script>
export default {
  props: ["singleRocket", "removeRocket"]
};
</script>

<style>
.rocket-images {
  width: 100px;
}
</style>