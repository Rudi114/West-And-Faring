<template lang="pug">
  div()
    img(src="../images/contact/cp_shadow.png" class="cp_shadow")
    h3(class="contact-title")
      | Contact
    p(class="contact-about")
      a(href="mailto:westandfaring1@gmail.com" class="the-styling")
        | westandfaring1@gmail.com
      br
      a(href="tel:925-451-4213" class="the-styling")
        | (925)451-4213
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
  @import url("https://use.typekit.net/zce0izl.css"); 

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
    font-size: 150px;
    height: auto;
    bottom: 90vh;
    left: 13.4vw;
    color: white;
    font-family: hero-new, sans-serif;
    font-weight: 100;
    font-style: normal;
    outline: 0;
    opacity: 0.59;
    letter-spacing: -10px;
  }
  .contact-about{
    position: relative;
    height: auto;
    bottom: 77vh;
    left: 14vw;
    color: white;
    font-size: 40px;
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
    border-bottom: none;
  }

  .the-styling{
    text-decoration: none;
    color: white;
  }

  @media only screen and (max-width: 830px) {
    .contact-title{
      font-size: 50px;
    }
    .contact-about{
      font-size: 21px;
    }
  }

   @media only screen and (max-width: 900px) and (max-height: 500px){
    .contact-title{
      font-size: 120px;
      bottom: 87vh;
    }
    .contact-about{
      font-size: 40px;
      bottom: 77vh;
      line-height: 60px;
    }
  }
</style>
