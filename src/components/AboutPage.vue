<template lang="pug">
  div
    div(class="current-section")
      h4(class="header color")
        | About
      h2(class="header-text color")
        | West&Faring is a community of designers, entrepeneurs, and developers aimed at transforming brands, solving problems, and improving people's lives
      img(src="../images/about/ap_burger.png" class="burger")
      img(src="../images/about/ap_shadow.png" class="shadow")
      div(class="grid-continer")
        img(src="../images/about/ap_plus.png" class="plus1")
        h3(class="creative-communication color")
          | Creative Communication
        p(class="creative_p")
          | We communicate complex ideas internally, with our clients, and with their audiences on a regular basis. Communication must be concise and effective in order to be successful. This is why we have developed creative ways to ensure that communication is being prioritised no matter who the conversation is between.
        img(src="../images/about/ap_plus.png" class="plus2")
        h3(class="curiosity color")
          | Curriosity
        p(class="curiosity_p font")
          | Steve Jobs told the world to ‘think different’. In order to do that, one must question everything. At West&Faring, curiosity is the driving force behind our problem solving process. We take advantage of first principles thinking through data and scrupulous testing. Once we have asked enough questions to determine the true nature of the problem, we solve it.
        img(src="../images/about/ap_plus.png" class="plus3")
        h3(class="innovation color")
          | Innovation
        p(class="innovation_p font")
          | At West&Faring, we work with creatives of all different backgrounds and disciplines to solve problems in unprecedented ways. We are a cross-functional team, gathering expertise in a variety of disciplines to attack a problem from many angles. Simply put, if you want to go fast, go alone. If you want to go far, go together. If you want to go fast and far, go with West&Faring.
        img(src="../images/about/ap_plus.png" class="plus4")
        h3(class="love color")
          | Love
        p(class="love_p font")
          | It’s quite simple, we absolutely love what we do. We know you will too. 
        img(src="../images/about/ap_join.png" class="join")

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
  .current-section{
    background: #4C64FF;
    height: 300vh;
  }

  .color{
    color: #FFFFE7;
    position: absolute;
  }

  .header{
    font-size: 30px;
    left: 9vw;
    top: 307vh;
  }

  .header-text{
    font-size: 40px;
    left: 9vw;
    top: 330vh;
    width: 140vh;
  }

  .burger{
    position: relative;
    width: 1cm;
    height: 0.4cm;
    display: block;
    margin-left: auto;
    margin-right: auto;
    top: 90vh;
  }

  .shadow{
    position: absolute;
    width: 30vw;
    right: 0vw;
    top: 300vh;
  }

  .grid-container{
    display: grid;
  }

  h3{
    font-size: 40px;
  }

  .creative-communication{
    position: absolute;
    left: 9vw;
    top: 403vh;
    height: 1cm;
    width: auto;
  }

  .curiosity{
    position: absolute;
    left: 9vw;
    top: 440vh;
    height: 1cm;
    width: auto;
  }

  .innovation{
    position: absolute;
    left: 9vw;
    top: 475vh;
    height: 1cm;
    width: auto;
  }

  .love{
    position: absolute;
    left: 9vw;
    top: 512vh;
    height: 1cm;
    width: auto;
  }

  p{
    color: #FFFFE7;
    font-family: hero-new, sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 20px;
  }

  .creative_p{
    position: absolute;
    left: 9vw;
    top: 411vh;
    width: 60vw;
  }

  .curiosity_p{
    position: absolute;
    left: 9vw;
    top: 448vh;
    width: 60vw;
  }

  .innovation_p{
    position: absolute;
    left: 9vw;
    top: 483vh;
    width: 60vw;
  }

  .love_p{
    position: absolute;
    left: 9vw;
    top: 520vh;
    width: 60vw;
  }

  .plus1{
    position: absolute;
    left: 43vw;
    top: 409.6vh;
    height: 0.5cm;
    width: auto;
  }

  .plus2{
    position: absolute;
    left: 43vw;
    top: 431.6vh;
    height: 0.5cm;
    width: auto;
  }

  .plus3{
    position: absolute;
    left: 43vw;
    top: 453.6vh;
    height: 0.5cm;
    width: auto;
  }

  .plus4{
    position: absolute;
    left: 43vw;
    top: 475.6vh;
    height: 0.5cm;
    width: auto;
  }

  .join{
    position: absolute;
    left: 43vw;
    top: 550vh;
    width: 14vw;
    height: auto;
  }
</style>
