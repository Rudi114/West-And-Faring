<template lang="pug">
  div
    v-col(cols="6")
      v-row
        v-img(src="../images/sticky_note/sn_exist.png" class="sn_exist" :style="{left: this.existLeft}")
        v-img(src="../images/sticky_note/sn_note.png" class="sn_note" :style="{right: this.noteRight}")
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
      this.noteRight =  '34vw'
      this.existLeft = '43.5vw'

    }
  }
}
</script>

<style lang="scss" scoped>
  div{
    background: #FFFEF4;
    height: 100vh;
  }
  .sn_note{
    background-color: transparent;
    position: absolute;
    top: 102.5vh;
    width: 65vw;
    right: 16.5vw;
    height: auto;
    z-index: 24;
    transition: all 0.7s;
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
