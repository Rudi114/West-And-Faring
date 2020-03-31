<template lang="pug">
  v-app(class="scroll-snap")
    ScrollDots(:scrollHeight="scrollHeight")
    //- vue-scroll-snap(:fullscreen="true")
    TitlePage(class="item" :scrollHeight="scrollHeight")
    StickyNotePage(class="item" :scrollHeight="scrollHeight")
    WorkPage(class="item")
    AboutPage(class="item")
    ContactPage(class="item")
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import VueScrollSnap from "vue-scroll-snap";

import ScrollDots from '@/components/ScrollDots.vue';
import TitlePage from '@/components/TitlePage.vue';
import StickyNotePage from '@/components/StickyNotePage.vue';
import WorkPage from '@/components/WorkPage.vue';
import AboutPage from '@/components/AboutPage.vue';
import ContactPage from '@/components/ContactPage.vue';
import ScrollSnap from '@/components/ScrollSnap.vue';

@Component({
  name: 'App',
  components: {
    ScrollDots,
    TitlePage,
    StickyNotePage,
    WorkPage,
    AboutPage,
    ContactPage,
    VueScrollSnap,
    ScrollSnap
  },
})
export default class App extends Vue {
  private scrollHeight: number = 0;

  public async mounted() {
		this.getScrollHeight();
    window.addEventListener('scroll', this.getScrollHeight);
  }

  private getScrollHeight() {
    this.scrollHeight = window.scrollY / window.innerHeight;
  }
}
</script>

<style lang="scss">
  .scroll-snap{
    scroll-behavior: smooth;
    width: 100vw;
    overflow-y: hidden;
    overflow-x: hidden;
  }
  html{
    overflow-y: hidden;
  }
  body{
    overflow-y: hidden;
  }
</style>
