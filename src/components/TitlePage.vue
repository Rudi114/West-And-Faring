<template lang="pug">
  div
    img(src="../images/title/tp_burger.png" class="tp_burger" :style="{opacity: this.opacity}")
</template>

<script lang="ts">
import { Component, Vue, Prop, Watch } from 'vue-property-decorator';

@Component({
  name: 'TitlePage',
  components: {},
})

export default class TitlePage extends Vue {
  @Prop() private scrollHeight!: number;

  private opacity: number = 1;

  @Watch('scrollHeight')
  onScroll() {
    this.opacity = 1 - 2 * this.scrollHeight;
  }
}
</script>

<style lang="scss" scoped>
  div{
    scroll-snap-align: start;
    background-image: url('../images/title/tp_title.png');
    background-size: cover;
    background-attachment: fixed;
    height: 100vh;
  }
  .tp_burger{
    position: relative;
    width: 3vw;
    height: 0.5cm;
    display: block;
    margin-left: auto;
    margin-right: auto;
    top: 90vh;
  }
</style>
