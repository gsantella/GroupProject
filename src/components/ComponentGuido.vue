<script setup>
  import {ref} from 'vue'
  const count = ref(0)
</script>

<template>
  <marquee>Guido</marquee>
  <h1>My counter = {{ money }}</h1>
  <h1>My counter * 10 = {{ count * 10 }}</h1>
  <p>This is a paragraph</p>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>

</style>
