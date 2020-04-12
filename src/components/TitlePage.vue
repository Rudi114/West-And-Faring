<template lang="pug">
  div(class="page")
    div(class="logo")
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
  // div{
  //   background-color: #f75b43;
  //   background-image: url('../images/title/tp_title.png');
  //   background-size: 100vw;
  //   background-attachment: fixed;
  //   height: 100vh;
  // }
  // .tp_burger{
  //   position: relative;
  //   width: 1cm;
  //   height: 0.4cm;
  //   display: block;
  //   margin-left: auto;
  //   margin-right: auto;
  //   top: 90vh;
  // }



  .page{
    background-color: #c94904;
  }
  .burger{
    position: relative;
    width: 1cm;
    height: 0.4cm;
    display: block;
    margin-left: auto;
    margin-right: auto;
    bottom: 10vh;
  }
  .logo{

    position: relative;
    background-color: #c94904;
    background-size: 100vw;
    background-image: url('../images/title/tp_logo.png');
    background-attachment: fixed;
    height: 100vh;
  }
</style>
