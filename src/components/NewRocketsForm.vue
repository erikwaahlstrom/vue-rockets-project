<template>
  <form @submit.prevent="onAddRocket">
    <label>Name</label>
    <input v-model="rocket.name" type="text" name="name" id="name" value />

    <label>Country</label>
    <input v-model="rocket.country" type="text" name="country" id="country" value />

    <label>Description</label>
    <textarea v-model="rocket.description" type="text" name="description" id="description"></textarea>

    <label>Image</label>
    <input v-model="rocket.image" type="text" name="image" id="image" value />

    <button type="submit">Add rocket</button>
  </form>
</template>

<script>
function getEmptyRocket() {
  return {
    name: "",
    description: "",
    country: "",
    image: ""
  };
}
export default {
  props: ["addRocket"],
  data: () => ({
    rocket: getEmptyRocket()
  }),
  methods: {
    onAddRocket() {
      this.addRocket(this.rocket);
      this.rocket = getEmptyRocket();
    }
  }
};
</script>

<style>
</style>