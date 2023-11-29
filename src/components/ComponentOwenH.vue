<script setup>
  import {ref} from 'vue'
  const count = ref(0)
</script>

<template>
  <h1>This is my special zone</h1>
  <p>This is a paragraph tag!</p>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>

</style>
