<template>
  <h1>Étape 2/3</h1>
  <p>(L'étape 1 sur la dimension de votre tringle a été validée.)</p>
  <div>
    <label for="message">{{ msg }}</label>
  </div>
  <div>
    Modèle DS <input type="radio" name="modele" v-model="message" /> Modèle RS
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