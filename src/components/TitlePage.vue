<template lang="pug">
  div
    p
    | Title
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'TitlePage',
  components: {
  },
})

export default class TitlePage extends Vue {
}
</script>

<style lang="scss" scoped>
  div{
    background-image: url('../images/title/tp_title.png');
    height: 100vh;
  }
</style>
