<script setup>
  function devin() { 
      alert("You fell into my trap")
      alert("Just three clicks away")
      alert("Only two to go!!!")
      alert("ONE MORE")
      alert("Sorry, i lied. Its the next one")
    while (true) {
    alert("CRAZY! I WAS CRAZY ONCE. THEY LOCKED ME IN A ROOM, A RUBBER ROOM, A RUBBER ROOM WITH RATS, AND RATS MAKE ME CRAZY.") 
    }
  }
  
</script>

<template>
  <h1>Devin</h1>
  <button @click="devin">Click me if you're crazy</button>
  <marquee>CLICK ME IF YOU'RE CRAZY</marquee>
  <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" class="button" target="_blank">Click this for good luck!</a>
</template>

<style scoped>
  h1 { background-color: crimson; }
  button { background-color: crimson; }
  marquee { background-color: crimson; }
  a { background-color: gold; }
</style>