<template lang="pug">
  div
    p
    | About
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'AboutPage',
  components: {
  },
})

export default class AboutPage extends Vue {
}
</script>

<style lang="scss" scoped>
  div{
    background: #4C64FF;
    height: 100vh;
  }
</style>
