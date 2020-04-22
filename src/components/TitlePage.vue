<template lang="pug">
  div(class="page")
    img(src="../images/title/logo_1.png" class="logo")
    img(src="../images/title/tp_burger.png" class="burger" :style="{opacity: this.opacity}")
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
  .page{
    background-color: #E75D46;
    overflow: hidden;
  }
  .burger{
    position: absolute;
    width: 1cm;
    height: 0.4cm;
    left: calc(50vw - 0.5cm);
    bottom: 10vh;
  }

  .logo{
    position: absolute;
    left: 15vw;
    width: 70vw;
    height: auto;
    top: 44%;
    transform: translateY(-50%);
  }
</style>
