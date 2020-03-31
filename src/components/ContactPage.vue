<template lang="pug">
  div()
    img(src="../images/contact/cp_shadow.png" class="cp_shadow")
    img(src="../images/contact/cp_temp.png" class="cp_temp")
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
  .cp_shadow{
    position: relative;
    height: 100vh;
    width: 100vw;
    top: 0vh;
  }
  .cp_temp{
    position: relative;
    width: 80vw;
    height: auto;
    bottom: 92vh;
    left: 9vw;
  }
</style>
