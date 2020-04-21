<template lang="pug">
  div(class="current-page")
    img(src="../images/contact/cp_shadow.png" class="cp_shadow")
    h3(class="contact-title")
      | Contact
    div(class="contact-form")
      input(v-model="name" placeholder="name" id="name" :style="{left: this.nameMove}" v-on:keyup.13='onEnter()')
      input(v-model="email" placeholder="email" id="email" :style="{left: this.emailMove}")
      textarea(v-model="message" placeholder="message" id="message" :style="{left: this.messageMove}")
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'ContactPage',
  components: {
  },
})

export default class ContactPage extends Vue {
  public nameMove: string = '14vw';
  private emailMove: string = '14vw';
  private messageMove: string = '14vw';
  public name: string = '';
  private email: string = ''
  private message: string = ''


  onEnter() {
    var input = document.getElementById("name");
    if(input !== null) {
      input.addEventListener("keyup", function(event) {
        if (event.keyCode === 13) {
          console.log('this far')
          event.preventDefault();
          var name = '28vw';
          return name;
        }
      });
      this.nameMove = name
      console.log(name)
    }
  }


}
</script>

<style lang="scss" scoped>
  .current-page{
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
    font-size: 80px;
    height: auto;
    bottom: 77vh;
    left: 14vw;
    color: white;
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
    text-decoration: none;
    outline: 0;
  }

  .contact-form{
    position: relative;
    width: 50vw;
    height: 50vh;
    bottom: 70vh;
    z-index: 43;
    color: white;
  }
  #name{
    position: relative;
    left: 14vw;
    background-color: grey;
    opacity: 0.5;
    border-radius: 10px;
    height: 30px;
    width: 300px;
    font-size: 30px;
  }

  #email{
    position: relative;
    left: 14vw;
    background-color: grey;
    opacity: 0.5;
    border-radius: 10px;
    height: 30px;
    width: 300px;
    font-size: 30px;
  }

  #message{
    position: relative;
    top: 5vh;
    left: 14vw;
    background-color: grey;
    opacity: 0.5;
    border-radius: 10px;
    height: 200px;
    width: 300px;
    font-size: 30px;
  }

  ::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
    color: white;
    opacity: 1; /* Firefox */
    align-self: start;
  }

  :-ms-input-placeholder { /* Internet Explorer 10-11 */
    color: white;
    align-self: start;
  }

  ::-ms-input-placeholder { /* Microsoft Edge */
    color: white;
    align-self: start;
  }


  @media only screen and (max-width: 830px) {
    .contact-title{
      font-size: 50px;
    }
  }

   @media only screen and (max-width: 900px) and (max-height: 500px){
    .contact-title{
      font-size: 120px;
      bottom: 87vh;
    }
  }
</style>
