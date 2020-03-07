<template lang="pug">
  div()
    p
    | Contact
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'ContactPage',
  components: {
  },
})

export default class ContactPage extends Vue {
}
</script>

<style lang="scss" scoped>
  div{
    background: #262B30;
    height: 100vh;
  }
</style>
