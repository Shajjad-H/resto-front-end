<template>
  <div class="center">
    <a :href="cardDetails.link" :target="cardDetails.link != '#/' ? '_blank' : '' ">
      <i class="material-icons large red-text text-darken-2 tooltipped" data-position="top" :data-tooltip="cardDetails.tooltip">{{cardDetails.icon}}</i>
    </a>
    <h4 class="flow-text">{{cardDetails.title}}</h4>
    <p v-html="cardDetails.desc" class="row"></p>
  </div>
</template>
<script>
export default {
  name: 'Card',
  props:{
    cardDetails: {
      type: Object
    }
  },
  mounted:function() {
    $('.tooltipped').tooltip();
  }
}

</script>
<style scoped>


</style>
