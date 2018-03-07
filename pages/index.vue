<template>
  <div class="content">

    <div class="name-about">
      <div class="name">
        <div class="logo">
          <span class="red name-letter letter">A</span>
          <span class="purple name-letter letter">L</span>
          <span class="bright-blue name-letter letter">I</span>
        </div>
        <div class="logo">
          <span class="dark-blue name-letter letter">S</span>
          <span class="blue name-letter letter">P</span>
          <span class="teal name-letter letter">I</span>
          <span class="green name-letter letter">T</span>
          <span class="yellow name-letter letter">T</span>
          <span class="pink name-letter letter">E</span>
          <span class="orange name-letter letter">L</span>
        </div>
      </div>

      <rainbow-text text="Ali Spittel"></rainbow-text>
      <p class="intro">I really like writing code.</p>
      <p class="intro">Especially in Python and JavaScript.</p>
      <p class="intro"><em>(click anywhere to interact)</em></p>
    </div>
  </div>
</template>

<script>
  import RainbowText from "../components/rainbow-text"

  export default {
    components: {
      'rainbow-text': RainbowText
    }
  }
</script>

<style>
</style>
