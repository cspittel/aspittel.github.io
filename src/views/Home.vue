<template>
  <div>
    <div class="v-center">
      <rainbow-text text="Ali Spittel" :large="true"></rainbow-text>

      <h2 class="intro">I really like writing code.</h2>
      <h2 class="intro">Especially in Python and JavaScript.</h2>
      <h2 class="intro"><a href="https://zen-of-programming.com/">Check Out My Blog!</a></h2>
      <h2 class="intro"><em>(click anywhere to interact)</em></h2>
    </div>
  </div>
</template>

<script>
  import RainbowText from "../components/RainbowText"

  export default {
    components: {
      'rainbow-text': RainbowText,
    }
  }
</script>

<style lang="scss">

  .intro {
    margin-bottom: -10px;
    font-size: 2em;
    font-weight: normal;
    color: #4A4A4A;

    @media (max-width: 650px) {
      font-size: 1.5em;
    }
  }


  .intro a {
    text-decoration: none;
    color: #2196f3;
  }

  .v-center {
    padding-top: 21vh;
  }
</style>
