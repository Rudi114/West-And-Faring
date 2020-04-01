<template lang="pug">
  div
    div(class="invisible-dot1")
    div(class="invisible-dot2")
    div(class="invisible-dot3")
    div(class="invisible-dot4")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-1 fade_in empty_dots" :style="{opacity: this.opacityLogo}")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-2 fade_in empty_dots" :style="{opacity: this.opacityLogo}")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-3 fade_in empty_dots" :style="{opacity: this.opacityLogo}")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-4 fade_in empty_dots" :style="{opacity: this.opacityLogo}")
    img(src="../images/scroll_dots/dot.png" class="sn-dot dots" :style="{opacity: this.opacityDot1}")
    img(src="../images/scroll_dots/dot.png" class="wp-dot dots" :style="{opacity: this.opacityDot2}")
    img(src="../images/scroll_dots/dot.png" class="ap-dot dots" :style="{opacity: this.opacityDot3}")
    img(src="../images/scroll_dots/dot.png" class="cp-dot dots" :style="{opacity: this.opacityDot4}")
    img(src="../images/scroll_dots/side_logo.png" class="side-logo" :style="{opacity: this.opacityLogo}")
</template>

<script lang="ts">
import { Component, Vue, Prop, Watch } from 'vue-property-decorator';

@Component({
  name: 'ScrollDots',
  components: {
  },
})

export default class ScrollDots extends Vue {
  @Prop() private scrollHeight!: number;

  private opacityDot1: number = 0;
  private opacityDot2: number = 0;
  private opacityDot3: number = 0;
  private opacityDot4: number = 0;
  private opacityLogo: number = 0;

  @Watch('scrollHeight')
  onScroll() {
    this.scrollHeight > 0.5 && this.scrollHeight <= 1.5 ? this.opacityDot1 = 1 : this.opacityDot1 = 0
    this.scrollHeight > 1.5 && this.scrollHeight <= 2.5 ? this.opacityDot2 = 1 : this.opacityDot2 = 0
    this.scrollHeight > 2.5 && this.scrollHeight <= 3.5 ? this.opacityDot3 = 1 : this.opacityDot3 = 0
    this.scrollHeight > 3.5 ? this.opacityDot4 = 1 : this.opacityDot4 = 0
    this.scrollHeight > 0.5 ? this.opacityLogo = 1 : this.opacityLogo = 0

  }
}
</script>

<style lang="scss" scoped>
  .empty_dots{
    position: fixed;
    width: 8px;
    height: auto;
    right: 6vw;
    mix-blend-mode: inherit;
    z-index: 1;
  }

  .single-empty-dot-1{
    top: 45.48vh;
  }

  .single-empty-dot-2{
    top: 48.29vh;
  }

  .single-empty-dot-3{
    top: 51vh;
  }

  .single-empty-dot-4{
    top: 53.61vh;
  }

  .invisible-dot1 {
    position: absolute;
    top: 90vh;
    height: 1vh;
  }

  .invisible-dot2 {
    position: absolute;
    top: 190vh;
    height: 1vh;
  }
  .invisible-dot3 {
    position: absolute;
    top: 290vh;
    height: 1vh;
  }
  .invisible-dot4 {
    position: absolute;
    top: 390vh;
    height: 1vh;
  }

  .dots {
    position: fixed;
    width: 8px;
    height: auto;
    right: 6vw;
    opacity: 1;
    z-index: 2;
  }

  .sn-dot{
    top: 45.48vh;
  }
  .wp-dot{
    top: 48.29vh;
  }

  .ap-dot{
    top: 51vh;
  }

  .cp-dot{
    top: 53.61vh;
  }
  .side-logo{
    position: fixed;
    top: 43vh;
    height: 3cm;
    width: 0.5cm;
    left: 4vw;
    mix-blend-mode: inherit;
  }
</style>
