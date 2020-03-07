<template lang="pug">
  div
    p
    | Sticky
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'StickyNotePage',
  components: {
  },
})

export default class StickyNotePage extends Vue {
}
</script>

<style lang="scss" scoped>
  div{
    background: #FFFEF4;
    height: 100vh;
  }
</style>
