<template lang="pug">
  div
    div(class="invisible-dot1")
    div(class="invisible-dot2")
    div(class="invisible-dot3")
    div(class="invisible-dot4")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-1 empty_dots" :style="{opacity: this.opacityDot}")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-2 empty_dots" :style="{opacity: this.opacityDot}")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-3 empty_dots" :style="{opacity: this.opacityDot}")
    img(src="../images/scroll_dots/single_empty_dot.png" class="single-empty-dot-4 empty_dots" :style="{opacity: this.opacityDot}")
    img(src="../images/scroll_dots/empty_dot_white.png" class="single-empty-dot-1 empty_dots" :style="{opacity: this.opacityDotWhite}")
    img(src="../images/scroll_dots/empty_dot_white.png" class="single-empty-dot-2 empty_dots" :style="{opacity: this.opacityDotWhite}")
    img(src="../images/scroll_dots/empty_dot_white.png" class="single-empty-dot-3 empty_dots" :style="{opacity: this.opacityDotWhite}")
    img(src="../images/scroll_dots/empty_dot_white.png" class="single-empty-dot-4 empty_dots" :style="{opacity: this.opacityDotWhite}")
    img(src="../images/scroll_dots/dot.png" class="sn-dot dots" :style="{opacity: this.opacityDot1}")
    img(src="../images/scroll_dots/dot.png" class="wp-dot dots" :style="{opacity: this.opacityDot2}")
    img(src="../images/scroll_dots/dot_white.png" class="ap-dot dots" :style="{opacity: this.opacityDot3}")
    img(src="../images/scroll_dots/dot.png" class="cp-dot dots" :style="{opacity: this.opacityDot4}")
    img(src="../images/scroll_dots/side_logo.png" class="side-logo" :style="{opacity: this.opacityLogo}")
    img(src="../images/scroll_dots/side_logo_white.png" class="side-logo" :style="{opacity: this.opacityLogoWhite}")

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

  private opacityDot: number = 0;
  private opacityDotWhite: number = 0;
  private opacityLogo: number = 0;
  private opacityLogoWhite: number = 0;

  @Watch('scrollHeight')
  onScroll() {
    this.scrollHeight > 0.5 && this.scrollHeight <= 1.5 ? this.opacityDot1 = 1 : this.opacityDot1 = 0;
    this.scrollHeight > 1.5 && this.scrollHeight <= 2.5 ? this.opacityDot2 = 1 : this.opacityDot2 = 0;
    this.scrollHeight > 2.5 && this.scrollHeight <= 5.5 ? this.opacityDot3 = 1 : this.opacityDot3 = 0;
    this.scrollHeight > 5.5 ? this.opacityDot4 = 1 : this.opacityDot4 = 0;
    ((this.scrollHeight > 0.5)  && (this.scrollHeight < 2.5)) || this.scrollHeight > 5.7 ? this.opacityDot = 1 : this.opacityDot = 0;
    (this.scrollHeight >= 2.5) && (this.scrollHeight <= 5.7) ? this.opacityDotWhite = 1 : this.opacityDotWhite = 0;
    ((this.scrollHeight > 0.5)  && (this.scrollHeight < 2.5)) || this.scrollHeight > 5.7 ? this.opacityLogo = 1 : this.opacityLogo = 0;
    (this.scrollHeight >= 2.5) && (this.scrollHeight <= 5.7) ? this.opacityLogoWhite = 1 : this.opacityLogoWhite = 0;
  }
}
</script>

<style lang="scss" scoped>
  .empty_dots{
    position: fixed;
    width: 8px;
    height: auto;
    right: 5vw;
    mix-blend-mode: inherit;
    z-index: 1;
    top: 50%;
    transform: translateY(-50%);
  }

  .single-empty-dot-1{
    // top: 45.48vh;
    transform: translateY(-30px);
  }

  .single-empty-dot-2{
    transform: translateY(-10px);
  }

  .single-empty-dot-3{
    transform: translateY(10px);
  }

  .single-empty-dot-4{
    transform: translateY(30px);
  }

  .dots {
    position: fixed;
    width: 8px;
    height: auto;
    right: 5vw;
    opacity: 1;
    z-index: 2;
    top: 50%;
    transform: translateY(-50%);
  }

  .sn-dot{
    transform: translateY(-30px);
  }
  .wp-dot{
    transform: translateY(-10px);
  }

  .ap-dot{
    transform: translateY(10px);
  }

  .cp-dot{
    transform: translateY(30px);
  }
  .side-logo{
    position: fixed;
    height: 98px;
    width: 0.5cm;
    left: 5vw;
    mix-blend-mode: inherit;
    top: 50%;
    transform: translateY(-50%);
  }
  // * {
  //   outline: 1px solid red;
  // }
</style>
