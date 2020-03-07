<template lang="pug">
  div
    p
    | Work
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'WorkPage',
  components: {
  },
})

export default class WorkPage extends Vue {
}
</script>

<style lang="scss" scoped>
  div{
    background: #FFFEF4;
    height: 100vh;
  }
</style>
