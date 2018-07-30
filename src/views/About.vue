<template>
  <div>
    <rainbow-text text="ABOUT"></rainbow-text>
    <div class="bio-pic">
      <img class="circular" src="../assets/pic.jpg" alt="selfie!">
      <div class="bio">
        <p>
          I have the really cool job of teaching other people how to code at <span class="highlighted-purple">General Assembly DC's</span>Web Development Immersive program. Before that, I was a software engineer at <span class="highlighted-blue">0ptimus</span>.
        </p>
        <p>
          I also <span><a href="https://zen-of-programming.com/">blog</a></span> a lot about code and my life as a developer.
        </p>
        <p>
          My favorite stack right now is <span class="highlighted-green">Vue.js</span> on the frontend and <span class="highlighted-pink">Django</span>          on the backend. I also have worked with React, Ruby on Rails, Java, Meteor, Express, MongoDB, PostgreSQL, CSS,
          and C++.
        </p>
        <p>
          When I'm not working you can find me watching my favorite New England sports teams, competing on CodeWars, taking runs around
          Capitol Hill, rock climbing, or participating in DC coding community events.
        </p>
        <p>
          I graduated from Hamilton College with a BA in government in 2016 after completing research in how to effectively teach computer
          science to 7-12th graders and on the differences in representation in Congress across party and gender lines.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import RainbowText from "@/components/RainbowText"

export default {
  components: {
    'rainbow-text': RainbowText,
  } 
}
</script>

<style lang="scss" scoped>
p {
  font-size: 18px;
}

.bio-pic {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  align-items: center;

  @media (max-width: 800px) {
    flex-direction: column;
  }
}

.circular {
  -ms-flex-item-align: center;
  margin-right: 40px;
  width: 300px;
  height: 300px;
  border-radius: 50%;
  float: left;
  margin-bottom: 20px;
  border: 15px solid #00bcd4;
  
  @media (max-width: 800px) {
    margin-right: 0px;
  }
}

.circular:hover {
  -ms-transform: rotate(360deg); 
  -webkit-transform: rotate(360deg);
  transform: rotate(360deg);
  -webkit-transition-duration: 3s;
  -moz-transition-duration: 3s;
  transition-duration: 3s;
}
</style>



