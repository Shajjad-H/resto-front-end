<template>
  <div class="row grey lighten-3">
    <div v-for="(card, i) in cardsDetails" :key="i"  class="col s12 m6 l4">
      <Card :cardDetails="card" />
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Cards",
  components: {
    Card
  },
  data() {
    return {
      cardsDetails: [
        {
          title: "Venez Sur Place",
          link: "https://goo.gl/maps/UXE8PEvdbHC2",
          icon: "room",
          tooltip: `Direction Google Map`,
          desc: `Le restaurant se situe au <br> 18 Route De Genas Villeurbanne.`
        },
        {
          title: "Commander Par Telephone",
          link: "tel:+3307070707",
          icon: "phone",
          tooltip: `Apellez le resto<br>07 07 07 07 07`,
          desc: `
                  Commandez au
                  <a href="tel:+000000" target="_blank" title="apeller"><strong><i class="red-text text-darken-3">00.00.00.00.00</i></strong></a>
                `
        },
        {
          title: "Commander en ligne",
          link: "#/",
          icon: "shopping_cart",
          tooltip: `Commander en ligne`,
          desc: `
                  <a href="https://www.just-eat.fr/" class="red btn btn-small waves-effect" target="_blank" title="allo resto"><i>JUST EAT</i></a>
                  <a href="https://www.just-eat.fr/" class="pink btn btn-small waves-effect" target="_blank" title="fodoora">FODOORA</a>
                  <a href="https://www.just-eat.fr/" class="green btn btn-small waves-effect" target="_blank" title="UBER EATS"><span class="black-text">UBER</span> EATS</a>
                `
        }
      ]
    };
  }
};
</script>
<style scoped>

</style>