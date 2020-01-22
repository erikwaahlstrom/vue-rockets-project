<template>
  <section>
    <new-rockets-form></new-rockets-form>
    <rocket-list></rocket-list>
  </section>
</template>

<script>
import NewRocketsForm from "../components/NewRocketsForm.vue";
import RocketList from "../components/RocketList.vue";

export default {
  name: "rockets",
  components: {
    NewRocketsForm,
    RocketList
  },
  async mounted() {
    this.$store.dispatch("getRockets");
  }
};
</script>

<style></style>
