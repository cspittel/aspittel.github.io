<template>
  <div class="header">
    <span v-for="(letter, index) in text" :key="index" class="letter" v-on:mouseover="hoverAnimation"> {{ letter }}</span>
  </div>
</template>

<script>
  export default {
    props: ['text'],
    methods: {
      hoverAnimation: (e) => {
        console.log(this)
        console.log(e)
      }
    }
  }
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css?family=Lato:400,800');
  
  .letter {
    font-family: 'Lato', sans-serif;
    font-weight: 800;
    letter-spacing: 20px;
    mix-blend-mode: darken;
    position: relative;
    -webkit-transition: top ease 0.1s;
    -o-transition: top ease 0.1s;
    transition: top ease 0.1s;
    -webkit-transition-delay: 2s;
    -o-transition-delay: 2s;
    transition-delay: 2s;
    opacity: 0.8;
    font-size: 20px;
    text-transform: uppercase;
  }
  
  .header span:nth-child(10n+1) {
    color: #ef5350;
  }
  
  .header span:nth-child(10n+2) {
    color: #ab47bc;
  }
  
  .header span:nth-child(10n+3) {
    color: #651fff;
  }
  
  .header span:nth-child(10n+4) {
    color: #3949ab;
  }
  
  .header span:nth-child(10n+5) {
    color: #2196f3;
  }
  
  .header span:nth-child(10n+6) {
    color: #00bcd4;
  }
  
  .header span:nth-child(10n+7) {
    color: #4caf50;
  }
  
  .header span:nth-child(10n+8) {
    color: #ffc107;
  }
  
  .header span:nth-child(10n+9) {
    color: #ff80ab;
  }
  
  .header span:nth-child(10n+10) {
    color: #ff8f00;
  }
  
  @media (max-width: 600px) {
    .letter {
        font-size: 20px;
        letter-spacing: 20px;
    }
  }

    @keyframes hoveranimation {
    0% {
      top: 0px;
    }
    50% {
      top: 20px;
    }
    100% {
      top: 0px;
    }
  }

  @-webkit-keyframes hoveranimation {
    0% {
      top: 0px;
    }
    50% {
      top: 20px;
    }
    100% {
      top: 0px;
    }
  }
  .hovered {
    -webkit-animation: hoveranimation 3s;
    animation: hoveranimation 3s;
  }
</style>

