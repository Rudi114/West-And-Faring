<template lang="pug">
  div(class="current-page")
    div(class="grid-container")
      a(v-bind:href="'https://www.behance.net/gallery/83719161/Winslet-Vineyards'")
        img(src="../images/work/wp_winslet1.png" class="wp-winslet portfolio-piece")
      a(v-bind:href="''")
        img(src="../images/work/wp_asu.png" class="wp-asu portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/90076107/Social-Packages'")
        img(src="../images/work/wp_db.png" class="wp-db portfolio-piece")
      a(v-bind:href="''")
        img(src="../images/work/wp_gaia.png" class="wp-gaia portfolio-piece")
      a(v-bind:href="''")
        img(src="../images/work/wp_quiksilver.png" class="wp-quiksilver portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/82852769/Logo-Book-1'")
        img(src="../images/work/wp_logo_book.png" class="wp-logo-book portfolio-piece")
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'WorkPage',
  components: {
  },
})

export default class WorkPage extends Vue {
}
</script>

<style lang="scss" scoped>
  .current-page{
    background: #FFFEF4;
    height: 100vh;
  }
  .grid-container{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-template-areas: 
      "top-left top-middle top-right"
      "bottom-left bottom-middle bottom-right";
  }
  .portfolio-piece{
    position: relative;
    width: 33vw;
    height: auto;
  }
  .wp-winslet{
    top: 15vh;
    left: 7vw;
    grid-area: top-left;
  }
  .wp-gaia{
    top: 3vh;
    left: 7vw;
    grid-area: bottom-left;
  }
  .wp-asu{
    top: 15vh;
    grid-area: top-middle;
  }
  .wp-quiksilver{
    top: 3vh;
    grid-area: bottom-middle;
  }
  .wp-db{
    top: 15vh;
    left: -7vw;
    grid-area: top-right;
  }
  .wp-logo-book{
    top: 3vh;
    left: -7vw;
    grid-area: bottom-right;
  }
  // * {
  //  outline: 1px solid red;
  // }
  
</style>
