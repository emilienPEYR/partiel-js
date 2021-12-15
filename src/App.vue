<template>
  <div><h1>Personnaliser ma tringle</h1></div>
  <Image />
  <div>
    <p>{{ price + price1 + price2 }}€ TTC</p>
  </div>
  <div v-if="step === 'step0'">
    <Dimension /> <br />
    <button
      v-on:click="
        step = 'step2';
        price = +80;
      "
    >
      Passer à la 2ème personnalisation
    </button>
  </div>
  <div v-if="step === 'step2'">
    <Modele msg="Quel modèle voulez-vous ?" /> <br />
    <button v-on:click="step = 'step0'">
      Revenir à la 1ère personnalisation</button
    ><br />
    <br />
    <button
      v-on:click="
        step = 'step3';
        price1 = +50;
      "
    >
      Passer à la 3ème personnalisation
    </button>
  </div>
  <div v-if="step === 'step3'">
    <Valider msg="Quel couleur voulez-vous ?" /> <br />
    <button v-on:click="step = 'step2'">
      Revenir à la 2ème personnalisation</button
    ><br />
    <br />
    <button v-on:click="price2 = +20">Valider</button>
    <button v-on:click="step = 'step4'">Ajouter au panier</button>
  </div>
  <div v-if="step === 'step4'">
    <h2>Votre tringle a été ajouter au panier.</h2>
    <button v-on:click="step = 'step0'; price = 0; price1 = 0; price2 = 0;">Acheter une nouvelle tringle ?</button>
  </div>
</template>

<script>
import Image from "./components/Image.vue";
import Dimension from "./components/Dimension.vue";
import Modele from "./components/Modele.vue";
import Valider from "./components/Valider.vue";

export default {
  name: "App",
  components: {
    Image,
    Dimension,
    Modele,
    Valider,
  },
  data() {
    return {
      step: "step0",
      price: 0,
      price1: 0,
      price2: 0,
    };
  },
};
</script>

<style>
div {
  text-align: center;
}
</style>
