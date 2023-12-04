<script setup>
    import {ref} from 'vue';
    const count = ref(0)
</script>

<template>
    <marquee>Marcus</marquee>
    <h1>Count * 10 = {{ count * 10 }}</h1>
    <p>This is a paragraph.</p>
    <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>
    
</style>
