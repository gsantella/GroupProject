<script setup>
  import {ref} from 'vue'
  const count = ref(0)
</script>

<template>
  <marquee>Adam</marquee>
  <p>This is a paragraph</p>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>

</style>