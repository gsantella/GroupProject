<script setup>
  import { ref, onMounted } from 'vue';

  const canvas = ref(null);
  let context = null;

  const colors = [
    "red",
    "blue",
    "green",
    "orange",
    "white",
    "purple",
    "yellow",
    "pink"
  ];

  const balls = ref([]);

  const settings = {
    ballSize: 25,
    ballAmount: 20, 
    maxDuration: 50
  }

  function randomNumber(n, s){
    return Math.floor(Math.random()*n)+s
  }

  function leftOrRight(){
    return randomNumber(2,0)
  }

  function updateBalls(){
    for (let i=0;i<balls.value.length;i++){
      if (balls.value[i].duration == 0){
        balls.value[i] = addBall();
        balls.value[i].duration = settings.maxDuration;
      }
      balls.value[i].duration -= 1;
      if (balls.value[i].dir == 0){
        balls.value[i].x -= balls.value[i].speed;
      } else {
        balls.value[i].x += balls.value[i].speed;
      }
    }
  }

  function createBalls(){
    for (let i = 0; i < settings.ballAmount; i++){
      balls.value.push(addBall());
    }
  }

  function drawBalls(){
    for (let i = 0; i < balls.value.length; i ++){
      context.beginPath();
      context.arc(balls.value[i].x,balls.value[i].y,balls.value[i].size,0,2*Math.PI);
      context.fillStyle = balls.value[i].color;
      context.fill();
    }
  }

  function addBall(){
    return {
      x: randomNumber(canvas.value.width - (settings.ballSize + 5), 1) + (settings.ballSize + 5),
      y: randomNumber(canvas.value.height - (settings.ballSize + 5), 1) + (settings.ballSize + 5),
      size: randomNumber(settings.ballSize, 5),
      color: colors[randomNumber(colors.length, 0)],
      duration: randomNumber(settings.maxDuration, 5),
      dir: leftOrRight(),
      speed: randomNumber(5,1)
    }
  }

  onMounted(() => {
    canvas.value = document.getElementById('canvas');
    context = canvas.value.getContext('2d');
    createBalls();
    function runCode(){
      context.clearRect(0,0,canvas.value.width,canvas.value.height);
      drawBalls();
      updateBalls();
      requestAnimationFrame(runCode);
    }
    runCode();
  });
</script>

<template>
  <canvas ref="canvas" id="canvas" height="400" width="600"></canvas>
</template>

<style scoped>
  canvas {
    background-color: black;
    width: 100%;
    height: 100%;
  }
</style>