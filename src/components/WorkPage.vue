<template lang="pug">
  div(class="current-page")
    div(class="grid-container")
      a(v-bind:href="'https://www.behance.net/gallery/83719161/Winslet-Vineyards'" class="wp-winslet portfolio-piece")
        img(src="../images/work/wp_winslet1.png" class="portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/94992987/ASU-Peer-to-Peer-Mentoring'" class="wp-asu portfolio-piece")
        img(src="../images/work/wp_asu.png" class="portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/90076107/Social-Packages'" class="wp-db portfolio-piece")
        img(src="../images/work/wp_db.png" class="portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/94626873/Gaia-Protection'" class="wp-gaia portfolio-piece")
        img(src="../images/work/wp_gaia.png" class="portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/94626579/Quiksilver-Rebrand'" class="wp-quiksilver portfolio-piece")
        img(src="../images/work/wp_quiksilver.png" class="portfolio-piece")
      a(v-bind:href="'https://www.behance.net/gallery/82852769/Logo-Book-1'" class="wp-logo-book portfolio-piece")
        img(src="../images/work/wp_logo_book.png" class="portfolio-piece")
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
    position: relative;
    top: 50%;
    transform: translateY(-50%);
    display: grid;
    grid-template-columns: 1fr 22vw 1fr 22vw 1fr;
    grid-template-rows: 1fr 13vh 1fr;
  }
  .portfolio-piece{
    width: 33vw;
    height: auto;
  }
  .wp-winslet{
    grid-column: 1 / span 2;
    grid-row: 1 / span 2;
    justify-self: end;
    align-self: end;
  }
  .wp-gaia{
    grid-column: 2 / span 3;
    grid-row: 1 / span 2;
    justify-self: center;
    align-self: end;
  }
  .wp-asu{
    grid-column: 4 / span 2;
    grid-row: 1 / span 2;
    justify-self: beginning;
    align-self: end;
  }
  .wp-quiksilver{
    grid-column: 1 / span 2;
    grid-row: 2 / span 2;
    justify-self: end;
    align-self: beginning;
  }
  .wp-db{
    grid-column: 2 / span 3;
    grid-row: 2 / span 2;
    justify-self: center;
    align-self: beginning;
  }
  .wp-logo-book{
    grid-column: 4 / span 2;
    grid-row: 2 / span 2;
    justify-self: beginning;
    align-self: beginning;
  }
  // * {
  //  outline: 1px solid red;
  // }
  
</style>
