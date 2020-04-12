<template lang="pug">
  div(class="page")
    v-img(src="../images/sticky_note/sn_exist.png" class="sn_exist" :style="{left: this.existLeft}")
    v-img(src="../images/sticky_note/sn_note.png" class="sn_note" :style="{left: this.noteRight}")
</template>

<script lang="ts">
import { Component, Vue, Prop, Watch } from 'vue-property-decorator';

@Component({
  name: 'StickyNotePage',
  components: {
  },
})

export default class StickyNotePage extends Vue {
  @Prop() private scrollHeight!: number;

  private noteRight: string = '16.5vw'
  private existLeft: string = '25vw'

  @Watch('scrollHeight')
  onScroll() {
    if(this.scrollHeight > 0.95) {
      this.noteRight =  '4vw'
      this.existLeft = '43.5vw'

    }
  }
}
</script>

<style lang="scss" scoped>
  .page{
    background: #FFFEF4;
    height: 100vh;
  }
  .sn_note{
    background-color: transparent;
    position: relative;
    width: 65vw;
    height: auto;
    z-index: 5;
    transition: all 0.7s;
    left: 30vw;
    top: 50%;
    transform: translateY(-50%);
  }
  .sn_exist{
    background-color: transparent;
    position: absolute;
    width: 50%;
    height: auto;
    left: 25vw;
    top: 125vh;
    z-index: 1;
    transition: all 0.7s;
  }
</style>
