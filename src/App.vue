<template lang="pug">
  v-app
    div(class="scroll-snap-container" id="scroll")
      ScrollDots(:scrollHeight="scrollHeight")
      TitlePage(class="scroll-item not-about" :scrollHeight="scrollHeight")
      StickyNotePage(class="scroll-item not-about" :scrollHeight="scrollHeight")
      WorkPage(class="scroll-item not-about")
      AboutPage(class="scroll-item about")
      ContactPage(class="scroll-item not-about")
</template>

<script lang="ts">
import { Component, Vue} from 'vue-property-decorator';

import ScrollDots from '@/components/ScrollDots.vue';
import TitlePage from '@/components/TitlePage.vue';
import StickyNotePage from '@/components/StickyNotePage.vue';
import WorkPage from '@/components/WorkPage.vue';
import AboutPage from '@/components/AboutPage.vue';
import ContactPage from '@/components/ContactPage.vue';

@Component({
  name: 'App',
  components: {
    ScrollDots,
    TitlePage,
    StickyNotePage,
    WorkPage,
    AboutPage,
    ContactPage,
  },
})
export default class App extends Vue {
  private scrollHeight: number = 0;

  public async mounted() {
    this.getScrollHeight();
    var element = document.getElementById("scroll")
    if (element !== null) {
      element.addEventListener('scroll', this.getScrollHeight);
    }
  }

  private getScrollHeight() {
    var element = document.getElementById("scroll")
    if (element !== null) {
      this.scrollHeight = element.scrollTop / window.innerHeight;
    }
    
  }
}
</script>

<style lang="scss">
    .scroll-snap-container {
    display: block;
    overflow-y: scroll;
    overflow-x: hidden;
    -webkit-overflow-scrolling: touch;
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    align-items: stretch;
    justify-content: flex-start;
    position: absolute;
    top: 0px;
    bottom: 0px;
    left: 0px;
    right: 0px;
    min-width: 100%;
    min-height: 100%;
  }
  .scroll-item {
    scroll-snap-align: start;
    scroll-snap-stop: always;
    flex: 1;
  }
  .about{
    height: 300vh;
  }

  .not-about{
    min-height: 100%;
  }
</style>
