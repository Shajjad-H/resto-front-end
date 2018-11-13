<template>
  <div>
    <div class="navbar-fixed z-depth-2">
      <nav>
        <div class="nav-wrapper red darken-3">
          <span class="left m-left">
            <a href="#" data-target="nav-mobile" class="sidenav-trigger">
              <i class="material-icons">menu</i>
            </a>
            <a href="#/" class="brand-logo flow-text waves-effect" @click="curPage = '/'">Bengal Tandoori</a>
          </span>
          <div class="container">
            <ul class="right hide-on-med-and-down">

              <li v-for="(page, i) in pages" :key="i" :class="{active: getCurPage === page}" @click="curPage=page" class="waves-effect ">
                  <a :href="'#' + page" v-html="getCurPageName(page)"></a>
              </li>

            </ul>
          </div>
        </div>
      </nav>
    </div>
    <ul id="nav-mobile" class="sidenav red darken-3">
      <li v-for="(page, i) in pages" :key="i" :class="{active: getCurPage === page}" @click="curPage=page" class="sidenav-close ">
        <a :href="'#' + page" class="white-text" v-html="getCurPageName(page)"></a>
      </li>
    </ul>

<!--
    <div class="fixed-action-btn">
      <a class="btn-floating btn-large red">
        <i class="material-icons">mode_edit</i>
      </a>
      <ul>
        <li><a class="btn-floating red"><i class="material-icons">insert_chart</i></a></li>
        <li><a class="btn-floating yellow darken-1"><i class="material-icons">format_quote</i></a></li>
        <li><a class="btn-floating green"><i class="material-icons">publish</i></a></li>
        <li><a class="btn-floating blue"><i class="material-icons">attach_file</i></a></li>
      </ul>
    </div>
-->
  </div>
</template>

<script>
import Slider from "./Slider.vue";

export default {
  name: "Header",
  data() {
    return {
      pages: ["/", "/Menu", "/Contact", "/Cart", "/User"],
      curPage: "/"
    };
  },
  computed: {
    getCurPage: function() {
      return this.curPage;
    }
  },
  components: {
    Slider
  },
  mounted: function() {
    $(".sidenav").sidenav({
      outDuration: 150,
    });
    
  },
  methods: {
    getCurPageName: function(pageUrl) {
      let pageName = pageUrl.split("/").pop();
      switch (pageName) {
        case "":
          return "Accueil";
        case "Cart":
          return `<i class="material-icons white-text">shopping_cart</i>`;
        case "User":
          return  `
                    <i class="material-icons white-text">account_box</i>

                  `;
        default:
          break;
      }
      return pageName;
    }
  }
};
/*<router-link to="/">Home</router-link>*/
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.text-justify {
  text-align: justify;
}

.text-left {
  text-align: left;
}

.brand-logo {
  font-size: 1.5em;
}

.m-left {
  margin-left: 1em;
}
</style>