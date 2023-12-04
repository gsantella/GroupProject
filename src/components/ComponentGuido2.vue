<script setup>
  import {ref} from 'vue'
  
  const props = defineProps({msg: {type: String, required: true}})
  const msg = ref(props.msg)

</script>

<template>
  <marquee>{{ msg }}</marquee>
</template>

<style scoped>

</style>
