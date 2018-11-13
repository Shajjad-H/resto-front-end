<template>
  <div class="margin-top-2">
    <div class="slider">
      <ul class="slides z-depth-3">
        <li v-for="(slide, i) in slides" :key="i">
          <img :src="slide.imgLink" alt="">
          <div class="caption center-align slider-text hide-on-small-only">
            <h4 class="slider-title">{{slide.title}}</h4>
            <p class="flow-text slider-desc white-text">{{slide.desc}}</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider",
  data() {
    return {
      slides: [
        {
          title: `This is our tagline`,
          imgLink: `https://photos.mandarinoriental.com/is/image/MandarinOriental/paris-2017-home?wid=2880&hei=1280&fmt=jpeg&crop=9,336,2699,1200&anchor=1358,936&qlt=75,0&fit=wrap&op_sharpen=0&resMode=sharp2&op_usm=0,0,0,0&iccEmbed=0&printRes=72`,
          desc: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum molestias mollitia dolor voluptas esse, repudiandae sint rem consectetur! Voluptate, alias.`
        },
        {
          title: `This is our tagline`,
          imgLink: `https://photos.mandarinoriental.com/is/image/MandarinOriental/paris-2017-home?wid=2880&hei=1280&fmt=jpeg&crop=9,336,2699,1200&anchor=1358,936&qlt=75,0&fit=wrap&op_sharpen=0&resMode=sharp2&op_usm=0,0,0,0&iccEmbed=0&printRes=72`,
          desc: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum molestias mollitia dolor voluptas esse, repudiandae sint rem consectetur! Voluptate, alias.`
        },
        {
          title: `This is our tagline`,
          imgLink: `https://photos.mandarinoriental.com/is/image/MandarinOriental/paris-2017-home?wid=2880&hei=1280&fmt=jpeg&crop=9,336,2699,1200&anchor=1358,936&qlt=75,0&fit=wrap&op_sharpen=0&resMode=sharp2&op_usm=0,0,0,0&iccEmbed=0&printRes=72`,
          desc: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum molestias mollitia dolor voluptas esse, repudiandae sint rem consectetur! Voluptate, alias.`
        }
      ]
    };
  },
  mounted: function() {
    $(".slider").slider();
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.text-justify {
  text-align: justify;
}
.text-left {
  text-align: left;
}
.red-text {
  color: red;
}
.slider-text{
  /*background-color: rgba(255, 0, 0, 0.5);*/
  text-align: center;
  border-radius: 0.5em;
  padding: 0.5em;
  color: white;
}
.slider-desc{
  text-align: justify;
  font-size: 1.5em;
}
.margin-top-2{
  margin-top: 0px;
}

</style>