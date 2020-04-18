<template lang="pug">
  div()
    img(src="../images/contact/cp_shadow.png" class="cp_shadow")
    h3(class="contact-title")
      | Contact
    p(class="contact-about")
      | email: westandfaring1@gmail.com
      br
      | phone: (925)451-4213
    //- img(src="../images/contact/cp_temp.png" class="cp_temp")
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
  .contact-title{
    position: relative;
    font-size: 70px;
    height: auto;
    bottom: 77vh;
    left: 14vw;
    color: white;
    font-family: hero-new, sans-serif;
    font-weight: 500;
    font-style: normal;
  }
  .contact-about{
    position: relative;
    height: auto;
    bottom: 67vh;
    left: 14vw;
    color: white;
    font-size: 30px;
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
  }

  @media only screen and (max-width: 830px) {
    .contact-title{
      font-size: 50px;
    }
    .contact-about{
      font-size: 21px;
    }
  }
</style>
