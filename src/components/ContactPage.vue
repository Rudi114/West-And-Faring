<template lang="pug">
  div(class="current-page")
    img(src="../images/contact/cp_shadow.png" class="cp_shadow")
    h3(class="contact-title")
      | Contact
    div(class="contact-form")
      input(v-model="name" placeholder="name" class="contact-input" id="name" :style="{right: this.nameMove}" v-on:keyup.13="nameOnEnter")
      input(v-model="company" placeholder="company" class="contact-input" id="company" :style="{right: this.companyMove}" v-on:keyup.13="companyOnEnter")
      input(v-model="email" placeholder="email" class="contact-input" id="email" :style="{right: this.emailMove}" v-on:keyup.13="emailOnEnter")
      input(v-model="message" placeholder="message" class="contact-input" id="message" :style="{right: this.messageMove}" v-on:keyup.13="messageOnEnter")
      div(class="thanks-div" :style="{right: this.thanksMove}")
        h2(class=("thanks"))
          | Thanks for reaching out!
        p(class="thanks-text")
          | You will hear from us soon.
</template>

<script lang="ts">
import { Component, Vue, Watch } from 'vue-property-decorator';

import emailjs from 'emailjs-com';

@Component({
  name: 'ContactPage',
  components: {
  },
})

export default class ContactPage extends Vue {
  public nameMove: string = '-33.2vw';
  public companyMove: string = '-150vw';
  private emailMove: string = '-150vw';
  private messageMove: string = '-150vw';
  private thanksMove: string = '-150vw';
  public name: string = '';
  public company: string = '';
  private email: string = '';
  private message: string = '';


  nameOnEnter() {
    this.nameMove = '100vw'
    this.companyMove = '-33.2vw'
    if(document.getElementById('name') !== null) {
      this.name = document.getElementById('name').value
      console.log(this.name)
    }
  }

  companyOnEnter() {
    this.companyMove = '100vw'
    this.emailMove = '-33.2vw'
  }

  emailOnEnter() {
    this.emailMove = '100vw'
    this.messageMove = '-33.2vw'
  }

  messageOnEnter() {
    this.messageMove = '100vw'
    this.thanksMove = '-14.2vw'

    var templateParams = {
      name: this.name,
      company: this.company,
      email: this.email,
      message: this.message
    };
 
    emailjs.send('default_service', 'template_XRt63hxT', templateParams, 'user_QovvQ4XnU3XT3d3Cw31Mw')
      .then(function(response) {
        console.log('SUCCESS!', response.status, response.text);
      }, function(error) {
        console.log('FAILED...', error);
      });
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
    font-size: 60px;
    height: auto;
    bottom: 90vh;
    left: 14vw;
    color: white;
    font-family: hero-new, sans-serif;
    font-weight: 100;
    font-style: normal;
    outline: 0;
    opacity: 0.59;
    letter-spacing: -10px;
  }

  .contact-form{
    position: relative;
    width: 50vw;
    height: 50vh;
    bottom: 70vh;
    z-index: 43;
    color: white;
  }
  .contact-input{
    position: absolute;
    bottom: 10vh;
    opacity: 0.5;
    border-bottom: 1px solid white;
    height: 150px;
    width: 70vw;
    font-size: 120px;
    font-family: hero-new, sans-serif;
    font-weight: 100;
    font-style: normal;
    transition: all 0.7s;
  }

  ::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
    color: white;
    opacity: 1; /* Firefox */
    align-self: start;
    // font-size: 60px;
  }

  :-ms-input-placeholder { /* Internet Explorer 10-11 */
    color: white;
    align-self: start;
  }

  ::-ms-input-placeholder { /* Microsoft Edge */
    color: white;
    align-self: start;
  }
  input, select { 
    outline: none;
  }

  .thanks-div{
    position: absolute;
    width: 50vw;
    bottom: 10vh;
    transition: all 0.7s;
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
  }

  .thanks{
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
    font-size: 40px;
  }

  .thanks-text{
    font-family: hero-new, sans-serif;
    font-weight: 300;
    font-style: normal;
  }


  @media only screen and (max-width: 830px) {
    .contact-title{
      font-size: 50px;
    }
    .contact-input{
      font-size: 80px;
    }
  }

   @media only screen and (max-width: 900px) and (max-height: 500px){
    .contact-title{
      font-size: 50px;
    }
    .contact-input{
      font-size: 80px;
      bottom: 20vh;
      height: 112px;
    }
  }
</style>
