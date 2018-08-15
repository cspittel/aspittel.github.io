<template>
  <div :class="{ large }">
    <span v-for="(letter, index) in text" :key="index">
      <rainbow-letter v-if="letter !== ' '" :letter="letter"></rainbow-letter>
      <br v-else>
    </span>
  </div>
</template>

<script>
  import RainbowLetter from './RainbowLetter'

  export default {
    props: ['text', 'large'],
    components: {
      'rainbow-letter': RainbowLetter
    } 
  }
</script>

<style lang="scss" scoped>
  @import url('https://fonts.googleapis.com/css?family=Lato:400,800');
    
  div span:nth-child(10n+1) > span {
    color: #ef5350;
  }
  
  div span:nth-child(10n+2) > span {
    color: #ab47bc;
  }
  
  div span:nth-child(10n+3) > span {
    color: #651fff;
  }
  
  div span:nth-child(10n+5) > span{
    color: #3949ab;
  }
  
  div span:nth-child(10n+4) > span {
    color: #2196f3;
  }
  
  div span:nth-child(10n+6) > span {
    color: #00bcd4;
  }
  
  div span:nth-child(10n+7) > span {
    color: #4caf50;
  }
  
  div span:nth-child(10n+8) > span {
    color: #ffc107;
  }
  
  div span:nth-child(10n+9) > span {
    color: #ff80ab;
  }
  
  div span:nth-child(10n+10) > span {
    color: #ff8f00;
  }

  div > span > span {
    font-size: 100px;
    letter-spacing: -10px;

    @media (max-width: 500px) {
      font-size: 80px;
    }
   @media (max-width: 400px) {
      font-size: 60px;
    }
  }

  .large > span > span {
    font-size: 250px;
    line-height: 60%;

    @media (max-width: 1050px) {
      font-size: 200px;
    }

    @media (max-width: 800px) {
      font-size: 150px;
    }

    @media (max-width: 650px) {
      font-size: 100px;
    }
    @media (max-width: 370px) {
      font-size: 80px;
    }
  }
</style>

