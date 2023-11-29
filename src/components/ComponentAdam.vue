<script setup>
  import {ref} from 'vue'
  const count = ref(0)
</script>

<template>
  <marquee>Adam</marquee>
  <h1>Mycounter = {{ count }}</h1>
  <h1>Mycounter = {{ count * 10}}</h1>
  <p>This is a paragraph</p>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>

</style>