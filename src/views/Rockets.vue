<template>
  <section>
    <new-rockets-form :addRocket="addRocket"></new-rockets-form>
    <rocket-list :rockets="rockets" :removeRocket="removeRocket"></rocket-list>
  </section>
</template>

<script>
import NewRocketsForm from "../components/NewRocketsForm.vue";
import RocketList from "../components/RocketList.vue";
import API from "../lib/API";
export default {
  name: "rockets",
  components: {
    NewRocketsForm,
    RocketList
  },

  async mounted() {
    this.rockets = await API.getRockets();
  },
  data: () => ({
    rockets: []
  }),
  methods: {
    addRocket(rocket) {
      this.rockets.push(rocket);
    },
    removeRocket(index) {
      this.rockets.splice(index, 1);
    }
  }
};
</script>

<style>
</style>