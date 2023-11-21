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

  //balls list
  const balls = ref([]);

  //ball object settings, change to user input
  const settings = {
    ballSize: 40,
    ballAmount: 100, 
    maxDuration: 100
  }

  //global random number
  function randomNumber(n, s){
    return Math.floor(Math.random()*n)+s
  }

  //update direction of balls
 function updateDirection() {
  for (let i = 0; i < balls.value.length; i++) {
    if ((balls.value[i].y + balls.value[i].dirY * balls.value[i].speed > canvas.value.height - balls.value[i].size) || (balls.value[i].y + balls.value[i].dirY * balls.value[i].speed < 0 + balls.value[i].size)) {
      balls.value[i].dirY = -balls.value[i].dirY;
    }
    if ((balls.value[i].x + balls.value[i].dirX * balls.value[i].speed > canvas.value.width - balls.value[i].size) || (balls.value[i].x + balls.value[i].dirX * balls.value[i].speed < 0 + balls.value[i].size)) {
      balls.value[i].dirX = -balls.value[i].dirX;
    }

    balls.value[i].y += balls.value[i].dirY * balls.value[i].speed;
    balls.value[i].x += balls.value[i].dirX * balls.value[i].speed;

    /*if (balls.value[i].dirY == 0){
      balls.value[i].y += balls.value[i].speed;
    } else {
      balls.value[i].y += balls.value[i].speed;
    }
    if (balls.value[i].dirx == 0){
      balls.value[i].x += balls.value[i].speed;
    } else {
      balls.value[i].x += balls.value[i].speed;
    }*/
    }
  }
  
  //base canvas of balls, checks ballsOnScreen == ballsAmount
  function createBalls(){
    for (let i = 0; i < settings.ballAmount; i++){
      balls.value.push(addBall());
    }
  }
  //draws all objects of balls[]  on canvas
  function drawBalls(){
    for (let i = 0; i < balls.value.length; i ++){
      context.beginPath();
      context.arc(balls.value[i].x,balls.value[i].y,balls.value[i].size,0,2*Math.PI);
      context.fillStyle = balls.value[i].color;
      context.fill();
    }
  }
  
  //returns values for ball object with specified values
  function addBall(){
    return {
      x: randomNumber(canvas.value.width - settings.ballSize, 0),
      y: randomNumber(canvas.value.height, 0),
      size: randomNumber(settings.ballSize, 5),
      color: colors[randomNumber(colors.length, 0)],
      dirX: randomNumber(2,1),
      dirY: randomNumber(2,1),
      speed: randomNumber(5,1)
    }
  }
  
  onMounted(() => {
    //sets value to 'canvas', get rendering element
    canvas.value = document.getElementById('canvas');
    context = canvas.value.getContext('2d');
    //generates balls
    createBalls();
    //clear canvas, draw balls, update, request frame, loop
    function runCode(){
      context.clearRect(0,0,canvas.value.width,canvas.value.height);
      drawBalls();
      updateDirection();
      //updatePosition();
      requestAnimationFrame(runCode);
    }
    //start loop
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