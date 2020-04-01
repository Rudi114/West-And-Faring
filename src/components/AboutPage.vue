<template lang="pug">
  div
    div(class="flex-div")
      img(src="../images/about/ap_love.png" class="ap_love")
      img(src="../images/about/ap_curiosity.png" class="ap_curiosity")
      img(src="../images/about/ap_creative_communication.png" class="ap_creative_communication")
      //- img(src="../images/about/ap_innovation.png" class="ap_innovation")
      img(src="../images/about/ap_join.png" class="ap_join")
      img(src="../images/about/ap_plus.png" class="plus1")
      img(src="../images/about/ap_plus.png" class="plus2")
      img(src="../images/about/ap_plus.png" class="plus3")
      img(src="../images/about/ap_plus.png" class="plus4")
      img(src="../images/about/ap_shadow.png" class="ap_shadow")
      p(class="ap_creative_p")
        | At West&Faring, we believe in breaking the mold and finding new ways to reach those who suppory your business
      p(class="ap_curiosity_p font")
        | Curiosity has driven human discovery for thousands of years. Why should that stop today? We believe that by facilitating that curiosity, we can discover amazing things
      p(class="ap_innovation_p font")
        | What keeps us ahead of our competitors is the fact that we dont get complacent. We constantly strive for innovative new ways to do what we do best
      p(class="ap_love_p font")
        | What makes mom's cooking so good? That same special ingrediant can be found from every logo to website that West&Faring creates
     

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

  .ap_creative_communication{
    position: absolute;
    left: 9vw;
    top: 308vh;
    height: 1cm;
    width: auto;
  }

  .ap_curiosity{
    position: absolute;
    left: 9vw;
    top: 330vh;
    height: 1cm;
    width: auto;
  }

  .ap_innovation{
    position: absolute;
    left: 9vw;
    top: 352vh;
    height: 1cm;
    width: auto;
  }

  .ap_love{
    position: absolute;
    left: 9vw;
    top: 374vh;
    height: 1cm;
    width: auto;
  }

  .ap_shadow{
    position: absolute;
    width: 30vw;
    right: 0vw;
  }

  .ap_join{
    position: absolute;
    left: 60vw;
    top: 350vh;
    width: 14vw;
    height: auto;
  }

  p{
    color: #FFFFE7;
    font-family: hero-new, sans-serif;
    font-weight: 400;
    font-style: normal;
  }

  .ap_creative_p{
    position: absolute;
    left: 9vw;
    top: 315vh;
    width: 35vw;
  }

  .ap_curiosity_p{
    position: absolute;
    left: 9vw;
    top: 337vh;
    width: 35vw;
  }

  .ap_innovation_p{
    position: absolute;
    left: 9vw;
    top: 359vh;
    width: 35vw;
  }

  .ap_love_p{
    position: absolute;
    left: 9vw;
    top: 381vh;
    width: 35vw;
  }

  .plus1{
    position: absolute;
    left: 43vw;
    top: 309.6vh;
    height: 0.5cm;
    width: auto;
  }

  .plus2{
    position: absolute;
    left: 43vw;
    top: 331.6vh;
    height: 0.5cm;
    width: auto;
  }

  .plus3{
    position: absolute;
    left: 43vw;
    top: 353.6vh;
    height: 0.5cm;
    width: auto;
  }

  .plus4{
    position: absolute;
    left: 43vw;
    top: 375.6vh;
    height: 0.5cm;
    width: auto;
  }
</style>
