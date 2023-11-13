<script setup>
  function clickMe() { 
    alert('I can not believe that you clicked the button. I am pretty sure that it said do not click me let me check. Yup it says do not click me and you clicked it anyways. Why? Why did you click the button? Do you always ignore directions?');
 }
</script>


<template>
  <h1><marquee>Gordon</marquee></h1>
  <button @click="clickMe()">Don't you dare click me</button>
</template>

<style scoped>
</style>



