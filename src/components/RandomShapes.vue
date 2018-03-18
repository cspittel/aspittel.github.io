<template>
  <canvas></canvas>
</template>

<script>
  import p5 from 'p5'

  function randomNumber (size) {
    return Math.floor(Math.random() * size)
  }

  function randomChoice (choices) {
    let index = randomNumber(choices.length)
    return choices[index]
  }

  const vueP5 = function (sketch) {

    let colors = []
    
    const numShapes = 3
    const maxSize = 200
    
    sketch.setup = () => {
      colors = [
        sketch.color(255, 143, 0, 80),
        sketch.color(255, 128, 171, 80),
        sketch.color(255, 193, 7, 80),
        sketch.color(76, 175, 80, 80),
        sketch.color(0, 188, 212, 80),
        sketch.color(171, 71, 188, 80),
        sketch.color(239, 83, 80, 80)
      ]
      sketch.createCanvas(window.innerWidth, document.body.offsetHeight)
      sketch.noStroke()
    }

    sketch.mouseClicked = () => {
      let sideLength = randomNumber(maxSize)
      sketch.fill(randomChoice(colors))
      let shapeType = randomNumber(numShapes)
      if (shapeType % numShapes == 0) {
        sketch.ellipse(sketch.mouseX, sketch.mouseY, sideLength, sideLength)
      } else if (shapeType % numShapes == 1) {
        sketch.rect(sketch.mouseX, sketch.mouseY, sideLength, sideLength)
      } else {
        sketch.triangle(sketch.mouseX, sketch.mouseY, sketch.mouseX + sideLength, sketch.mouseY,
          sketch.mouseX + (0.5 * sideLength), sketch.mouseY - sideLength)
      }
    }
  }

  export default {
    mounted () {
      const canvas = new p5(vueP5, 'vueP5')
    }
  }
</script>

<style lang="scss">
  canvas {
    position: fixed;
    top: 0;
    z-index: -1;
    width: 100%;
    height: 100vh;
    margin-left: 0em;
  }
</style>

