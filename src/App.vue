<template lang="pug">
  v-app
    div(class="scroll-snap-container" id="scroll" :class="{ scroll_mobile: mobile }")
      ScrollDots(:scrollHeight="scrollHeight" :pageWidth="pageWidth")
      TitlePage(class="scroll-item not-about" :scrollHeight="scrollHeight")
      StickyNotePage(class="scroll-item not-about" :scrollHeight="scrollHeight")
      WorkPage(class="scroll-item not-about")
      AboutPage(class="scroll-item about")
      ContactPage(class="scroll-item not-about")
      div( v-if="(pageWidth < 800) && (mobile === true)" class="rotate")
        img( v-if="(pageWidth < 800) && (mobile === true)" src="./images/mobile/rotate.png" class="rotate-img")
</template>

<script lang="ts">
import { Component, Vue, Watch } from 'vue-property-decorator';

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
  private pageWidth: number = 1152;
  private mobile: boolean = false;

  @Watch('scrollHeight')
  public setSnap(scrollHeight: number) {
    var element = document.getElementById("scroll")
    if ((element !== null) && (this.scrollHeight < 2.99)) {
      element.setAttribute("style", "scroll-snap-type: y mandatory")
    } else if (element !== null) {
      element.setAttribute("style", "scroll-snap-type: y proximity")
    }
  }

  public async mounted() {
    this.getScrollHeight();
    var element = document.getElementById("scroll")
    if (element !== null) {
      element.addEventListener('scroll', this.getScrollHeight);
    }
  }

  public created() {
    this.setWidth()
    window.addEventListener('resize', this.setWidth);
  }

  private getScrollHeight() {
    var element = document.getElementById("scroll")
    if (element !== null) {
      this.scrollHeight = element.scrollTop / window.innerHeight;
    }
  }

  public setWidth() {
    this.pageWidth = window.innerWidth;
    console.log(this.pageWidth)
    if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|BB|PlayBook|IEMobile|Windows Phone|Kindle|Silk|Opera Mini/i.test(navigator.userAgent)) {
      this.mobile = true
      console.log("true")
    } else {
      this.mobile = false
      console.log("false")
    }
  }
}
</script>

<style lang="scss">
    .scroll-snap-container {
    display: block;
    overflow-y: scroll;
    overflow-x: hidden;
    // -webkit-overflow-scrolling: touch;
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
    height: 320vh;
  }

    @media only screen and (max-width: 1030px) {
      .about{
        height: 320vh;
      }
    }

    @media only screen and (max-width: 930px) {
      .about{
        height: 340vh;
      }
    }

    @media only screen and (max-width: 830px) {
      .about{
        height: 340vh;
      }
    }

    @media only screen and (max-width: 830px) and (max-height: 500px){
      .about{
        height: 370vh;
      }
    }

  .not-about{
    min-height: 100%;
  }

  .rotate{
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    opacity: 1;
    background-color: black;
    z-index: 7;
  }

  .rotate-img{
    position: relative;
    top: 25vh;
    left: 10vw;
    height: 80vw;
  }

  @media only screen and (orientation: portrait) {
    .rotate{
      opacity: 1;
      background-color: black;
    }

    .scroll-mobile{
      overflow: hidden;
    }
  }


</style>
