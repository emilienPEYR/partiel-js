<template>
  <div id="app">
    <h1>Axios - point bonus</h1>
    <div v-for="info in info" :key="info" class="currency">
      {{ Object.keys(info)[0] }} <br>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "HelloWorld",
  data() {
    return {
      info: null,
    };
  },
  mounted() {
    axios
      .get("https://calendrier.api.gouv.fr/jours-feries/metropole.json")
      .then((response) => (this.info = response));
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
