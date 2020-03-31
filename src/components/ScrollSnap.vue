<template lang="pug">
  div(class="scroll-snap-container")
    slot
</template>

<script lang="ts">
import { Component, Vue, Prop, Watch } from 'vue-property-decorator';

@Component({
  name: 'ScrollSnap',
  components: {},
})

export default class ScrollSnap extends Vue {
}
</script>

<style lang="scss" scoped>
  .scroll-snap-container{
    scroll-snap-type: y mandatory;
  }

</style>