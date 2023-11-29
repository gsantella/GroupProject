
<script setup>
  import {ref} from 'vue'
   const count = ref(0)
</script>

<template>
  <h1>Ben</h1>
  <h1> My counter = {{ count }}</h1>
  <h1> My counter = {{ count * 10 / 5 }}</h1>
  <p>This is a paragraph</p>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>
h1 {
  color: #FA8072;  
}
</style>