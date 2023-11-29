<script setup>
  import {ref} from 'vue'
  const count = ref(0)
</script>

<template>
  <h1>This is my special zone</h1>
  <p>This is a paragraph tag!</p>
  <h2>My button has been clicked {{ count }} times!</h2>
  <button @click="count++">BUTTON</button>
</template>

<style scoped>

</style>
