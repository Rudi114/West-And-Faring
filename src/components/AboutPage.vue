<template lang="pug">
  div
    link(rel="stylesheet" href="https://use.typekit.net/zce0izl.css")
    div(class="current-section")
      h4(class="header color")
        | About
      p(class="header-text color")
        | West&Faring is a community of designers, entrepeneurs, and developers aimed at transforming brands, solving problems, and improving people's lives.
      img(src="../images/about/ap_shadow.png" class="shadow")
      img(src="../images/about/burger_2.png" class="burger")
      p(class="believe")
        | What we believe
      div(class="grid-container")
        img(src="../images/about/ap_plus.png" class="plus1")
        h3(class="creative-communication color")
          | Creative Communication
        p(class="creative_p font p_width")
          | We communicate complex ideas internally, with our clients, and with their audiences on a regular basis. Communication must be concise and effective in order to be successful. This is why we have developed creative ways to ensure that communication is being prioritised no matter who the conversation is between.
        img(src="../images/about/ap_plus.png" class="plus2")
        h3(class="curiosity color")
          | Curiosity
        p(class="curiosity_p font p_width")
          | Steve Jobs told the world to ‘think different’. In order to do that, one must question everything. At West&Faring, curiosity is the driving force behind our problem solving process. We take advantage of first principles thinking through data and scrupulous testing. Once we have asked enough questions to determine the true nature of the problem, we solve it.
        img(src="../images/about/ap_plus.png" class="plus3")
        h3(class="innovation color")
          | Innovation
        p(class="innovation_p font p_width")
          | At West&Faring, we work with creatives of all different backgrounds and disciplines to solve problems in unprecedented ways. We are a cross-functional team, gathering expertise in a variety of disciplines to attack a problem from many angles. Simply put, if you want to go fast, go alone. If you want to go far, go together. If you want to go fast and far, go with West&Faring.
        img(src="../images/about/ap_plus.png" class="plus4")
        h3(class="love color")
          | Love
        p(class="love_p font p_width")
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
    position: absolute;
    left: calc(50vw - 75px);
    top: 605vh;
    width: 150px;
    padding: 0;
    margin: 0;
    height: auto;
  }

  .current-section{
    background: #4C64FF;
    height: 340vh;
  }

  .color{
    color: #FFFFE7;
    position: absolute;
  }

  .header{
    font-size: 30px;
    left: 14vw;
    top: 307vh;
    font-family: hero-new, sans-serif;
    font-weight: 400;
    font-style: normal;
    align-self: center;
  }

  .header-text{
    font-size: 40px;
    left: 14vw;
    top: 326vh;
    width: 65vw;
    font-family: hero-new, sans-serif;
    font-weight: 600;
    font-style: normal;
    line-height: 56px;
    letter-spacing: -1px;
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
    color: #FFFFE7;
  }

  .believe{
    position: relative;
    top: 100vh;
    font-size: 30px;
    text-align: center;
  }

  h3{
    font-size: 40px;
    font-family: hero-new, sans-serif;
    font-weight: 500;
    font-style: normal;
    margin-bottom: 15px;
  }

  .grid-container{
    position: relative;
    top: 115vh;
    left: 14vw;
    height: 170vh;
    width: 55vw;
    display: grid;
    grid-template-columns: 11fr 2fr;
    grid-template-rows: 100px 5fr 1fr 100px 6fr 1fr 100px 6fr 1fr 100px 4fr;
  }

  .p_width{
    width: 50vw;
  }

    @media only screen and (max-width: 1030px) {
      .header-text{
        font-size: 36px;
      }
      .grid-container{
        height: 180vh;
        width: 55vw;
        grid-template-columns: 8fr 1fr;
        grid-template-rows: 80px 5fr 1fr 80px 6fr 1fr 80px 6fr 1fr 80px 4fr;
      }
      .current-section{
        height: 360vh;
      }
      .join{
        top: 630vh;
      }
      h3{
        font-size: 35px;
      }
      .p_width{
        width: 50vw;
      }
    }

    @media only screen and (max-width: 930px) {
      .header-text{
        font-size: 31px;
        line-height: 47px;
      }
      .grid-container{
        height: 190vh;
        width: 55vw;
        grid-template-columns: 8fr 1fr;
        grid-template-rows: 70px 5fr 1fr 70px 6fr 1fr 70px 6fr 1fr 70px 4fr;
      }
      .current-section{
        height: 360vh;
      }
      .join{
        top: 625vh;
      }
      h3{
        font-size: 30px;
      }
      .p_width{
        width: 50vw;
      }
    }

    @media only screen and (max-width: 830px) {
      .header-text{
        font-size: 26px;
        line-height: 38px;
      }
      .grid-container{
        height: 180vh;
        width: 75vw;
        grid-template-columns: 8fr 1fr;
        grid-template-rows: 70px 5fr 1fr 70px 6fr 1fr 70px 6fr 1fr 70px 4fr;
      }
      .current-section{
        height: 360vh;
      }
      .join{
        top: 615vh;
      }
      h3{
        font-size: 25px;
      }
      .p_width{
        width: 70vw;
      }
    }


    @media only screen and (max-width: 900px) and (max-height: 500px){
      .header-text{
        font-size: 35px;
        line-height: 44px;
      }
      .grid-container{
        height: 220vh;
        width: 75vw;
        grid-template-columns: 8fr 1fr;
        grid-template-rows: 60px 5fr 1fr 60px 6fr 1fr 60px 6fr 1fr 60px 4fr;
      }
      .current-section{
        height: 390vh;
      }
      .join{
        top: 655vh;
      }
      h3{
        font-size: 25px;
      }
      .p_width{
        width: 70vw;
      }
    }


  .creative-communication{
    grid-column: 1 / span 2;
    grid-row: 1 / span 1;
    height: 1cm;
    width: auto;
    align-self: center;
  }

  .curiosity{
    grid-column: 1 / span 2;
    grid-row: 4 / span 1;
    height: 1cm;
    width: auto;
    align-self: center;
  }

  .innovation{
    grid-column: 1 / span 2;
    grid-row: 7 / span 1;
    height: 1cm;
    width: auto;
    align-self: center;
  }

  .love{
    grid-column: 1 / span 2;
    grid-row: 10 / span 1;
    height: 1cm;
    width: auto;
    align-self: center;
  }

  p{
    color: #FFFFE7;
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
    font-size: 17px;
  }

  .creative_p{
    grid-column: 1 / span 1;
    grid-row: 2 / span 2;
  }

  .curiosity_p{
    grid-column: 1 / span 1;
    grid-row: 5 / span 2;
  }

  .innovation_p{
    grid-column: 1 / span 1;
    grid-row: 8 / span 2;
  }

  .love_p{
    grid-column: 1 / span 1;
    grid-row: 11 / span 2;
  }

  .plus1{
    grid-column: 2 / span 1;
    grid-row: 1 / span 1;
    align-self: center;
    height: 0.7cm;
    width: auto;
  }

  .plus2{
    grid-column: 2 / span 1;
    grid-row: 4 / span 1;
    align-self: center;
    height: 0.7cm;
    width: auto;
  }

  .plus3{
    grid-column: 2 / span 1;
    grid-row: 7 / span 1;
    align-self: center;
    height: 0.7cm;
    width: auto;
  }

  .plus4{
    grid-column: 2 / span 1;
    grid-row: 10 / span 1;
    align-self: center;
    height: 0.7cm;
    width: auto;
  }
</style>
