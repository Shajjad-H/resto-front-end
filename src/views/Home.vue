<template>
  <div class="home">
    <Slider />
    <Cards />
    <Map />
  </div>
</template>

<script>
// @ is an alias to /src
import Slider from '@/components/Slider.vue';
import Cards from '@/components/Home/Cards.vue';
import Map from '@/components/Map.vue';

export default {
  name: 'home',
  components: {
    Slider,
    Cards,
    Map
  }
}
</script>
<style scoped>



</style>

