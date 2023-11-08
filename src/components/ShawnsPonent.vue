<script setup>
function guidoButton(){
  document.getElementById("add_message").innerHTML = "<marquee>Guido<marquee/>"
}
  
</script>

<template>
  <button id ="add_message" @click="guidoButton()">Add Message</button>
</template>

<style scoped>

  
</style>