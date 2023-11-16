<script setup>
  let count = 0
  function increment() {
  document.getElementById("clicker").innerHTML = "You shouldn't have clicked me " + count + " times" ;
    count--;
  }

</script>

<template>
  <h1><marquee>This is Daniel's button no touch</marquee></h1>
  <button id="clicker" @click="increment()">Button</button>




</template>

<style scoped>
h1 {
  color: darkblue;
}
button {
align: center;
}
</style>

