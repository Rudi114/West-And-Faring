<template lang="pug">
  div
    div(class="current-section")
      h4(class="header color")
        | About
      h2(class="header-text color")
        | West&Faring is a community of designers, entrepeneurs, and developers aimed at transforming brands, solving problems, and improving people's lives
      img(src="../images/about/ap_shadow.png" class="shadow")
      img(src="../images/about/ap_burger.png" class="burger")
      p(class="believe")
        | What we believe
      div(class="grid-container")
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
  @import url("https://use.typekit.net/zce0izl.css");

  .join{
    position: relative;
    left: 33vw;
    top: 140vh;
    width: 14vw;
    height: auto;
  }

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

  .shadow{
    position: absolute;
    width: 30vw;
    right: 0vw;
    top: 300vh;
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

  .believe{
    position: relative;
    top: 100vh;
    left: 40vw;
    font-size: 30px;
  }

  .grid-container{
    position: relative;
    top: 115vh;
    left: 10vw;
    height: 120vh;
    width: 80vw;
    display: grid;
    grid-template-columns: 9fr 1fr;
    grid-template-rows: 4fr 4fr 1fr 4fr 4fr 1fr 4fr 4fr 1fr 4fr 4fr;
    grid-template-areas: 
      "one-top-left one-top-right"
      "one-bottom one-bottom"
      ". ."
      "two-top-left two-top-right"
      "two-bottom two-bottom"
      ". ."
      "three-top-left three-top-right"
      "three-bottom three-bottom"
      ". ."
      "four-top-left four-top-right"
      "four-bottom four-bottom";
  }

    @media only screen and (max-width: 1030px) {
      .header-text{
        font-size: 30px;
      }
      .grid-container{
        height: 147vh;
      }
      .current-section{
        height: 327vh;
      }
      .join{
        top: 167vh;
      }
    }

    @media only screen and (max-width: 930px) {
      .header-text{
        font-size: 25px;
      }
      .grid-container{
        height: 174vh;
      }
      .current-section{
        height: 354vh;
      }
      .join{
        top: 194vh;
      }
    }

    @media only screen and (max-width: 830px) {
      .header-text{
        font-size: 20px;
      }
      .grid-container{
        height: 200vh;
      }
      .current-section{
        height: 380vh;
      }
      .join{
        top: 220vh;
      }
    }


  h3{
    font-size: 40px;
    font-family: hero-new, sans-serif;
    font-weight: 500;
    font-style: normal;
  }

  .creative-communication{
    grid-area: one-top-left;
    height: 1cm;
    width: auto;
  }

  .curiosity{
    grid-area: two-top-left;
    height: 1cm;
    width: auto;
  }

  .innovation{
    grid-area: three-top-left;
    height: 1cm;
    width: auto;
  }

  .love{
    grid-area: four-top-left;
    height: 1cm;
    width: auto;
  }

  p{
    color: #FFFFE7;
    font-family: hero-new, sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 15px;
  }

  .creative_p{
    grid-area: one-bottom;
    width: 60vw;
  }

  .curiosity_p{
    grid-area: two-bottom;
    width: 60vw;
  }

  .innovation_p{
    grid-area: three-bottom;
    width: 60vw;
  }

  .love_p{
    grid-area: four-bottom;
    width: 60vw;
  }

  .plus1{
    grid-area: one-top-right;
    align-self: center;
    height: 0.5cm;
    width: auto;
  }

  .plus2{
    grid-area: two-top-right;
    align-self: center;
    height: 0.5cm;
    width: auto;
  }

  .plus3{
    grid-area: three-top-right;
    align-self: center;
    height: 0.5cm;
    width: auto;
  }

  .plus4{
    grid-area: four-top-right;
    align-self: center;
    height: 0.5cm;
    width: auto;
  }
</style>
