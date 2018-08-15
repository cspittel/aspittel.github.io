<template>
  <div class="links">
    <a href="https://twitter.com/ASpittel" class="social-link" title="Twitter"><i class="fa fa-twitter blue" aria-hidden="true"></i></a>
    <a href="https://dev.to/aspittel" class="social-link dev-to">
      <img src="https://d2fltix0v2e0sb.cloudfront.net/dev-badge.svg" alt="Ali Spittel's DEV Profile" class="dev-to-img"/>
    </a>
    <a href="https://github.com/aspittel" class="social-link" title="Github"><i class="fa fa-github purple" aria-hidden="true"></i></a>
    <a href="https://www.linkedin.com/in/ali-spittel-768a98119" class="social-link" title="Linkedin"><i class="fa fa-linkedin dark-blue" aria-hidden="true"></i></a>
    <a href="mailto:ali07cat07@gmail.com" class="social-link" title="email me"><i class="fa fa-envelope red" aria-hidden="true"></i></a>
    <a href="https://instagram.com/ali_writes_code" class="social-link" title="Instagram"><i class="fa fa-instagram pink" aria-hidden="true"></i></a> 
    <a href="https://zen-of-programming.com" class="social-link" title="Blog"><i class="fa fa-link green" aria-hidden="true"></i></a>
  </div>
</template>

<style lang="scss" scoped>
.links {
  text-align: center;
  position: fixed;
  bottom: 0px;
  width: 90%;
  background-color: white;
  padding-bottom: 5%
}

.social-link {
  font-size: 30px;
  margin-right: 25px;

  @media (max-width: 700px) {
    margin-right: 15px;
  }
}

.dev-to {
  margin-top: 5px;
}

.dev-to-img {
  height: 25px;
  width: 25px;
}
.social-link:hover {
  opacity: 0.5;
}

.red {
  color: #ef5350;
}

.purple {
  color: #ab47bc;
}

.bright-blue {
  color: #651fff;
}

.dark-blue {
  color: #3949ab;
}

.blue {
  color: #2196f3;
}

.teal {
  color: #00bcd4;
}

.green {
  color: #4caf50;
}

.yellow {
  color: #ffc107;
}

.pink {
  color: #ff80ab;
}

.orange {
  color: #ff8f00;
}
</style>

