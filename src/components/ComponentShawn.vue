<script setup>
function guidoButton(){
  document.getElementById("add_message").innerHTML = "<marquee>Guido<marquee/>"
}
  
</script>

<template>
  <button id ="add_message" @click="guidoButton()">Add Message</button>
  
</template>

<style scoped>
button{
  background-color: pink;
  text-align: centert;
  width: 700px;
  height: 500 px;
  font-size: 90pt;
  border-width: 17px;
  

}

  
</style>