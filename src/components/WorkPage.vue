<template lang="pug">
  div
    img(src="../images/work/wp_winslet.png" class="wp-winslet portfolio-piece")
    img(src="../images/work/wp_asu.png" class="wp-asu portfolio-piece")
    img(src="../images/work/wp_db.png" class="wp-db portfolio-piece")
    img(src="../images/work/wp_gaia.png" class="wp-gaia portfolio-piece")
    img(src="../images/work/wp_quiksilver.png" class="wp-quiksilver portfolio-piece")
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
  div{
    scroll-snap-align: start;
    background: #FFFEF4;
    height: 100vh;
  }
  .portfolio-piece{
    position: relative;
    width: 33vw;
    height: auto;
  }
  .wp-winslet{
    top: 15vh;
    left: 7vw;
  }
  .wp-gaia{
    top: 3vh;
    left: 7vw;
  }
  .wp-asu{
    top: 15vh;
  }
  .wp-quiksilver{
    top: 3vh;
  }
  .wp-db{
    top: 15vh;
    left: -7vw;
  }
  .wp-logo-book{
    top: 3vh;
    left: -7vw;
  }
  
</style>
