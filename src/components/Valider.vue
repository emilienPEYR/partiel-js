<template>
  <h1>Étape 3/3</h1>
  <p>(L'étape 1 et 2 ont été validé.)</p>
  <div>
    <label for="message">{{ msg }}</label>
  </div>
  <div>
    Noir <input type="radio" name="modele" v-model="message" v-on:click="step = 'step4'"/> Blanc
    <input type="radio" name="modele" />
  </div>
</template>

<script>
export default {
  name: "Competences",
  props: {
    msg: String,
  },
  
};
</script>

<style scoped>
</style>