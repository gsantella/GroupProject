<script setup>
    import {ref, defineEmits} from 'vue';

    const emit = defineEmits(['bigError']);
    const count = ref(0);
</script>

<template>
    <button @click="$emit('bigError')">Emit Event</button>
    <marquee>Marcus</marquee>
    <h1>Count * 10 = {{ count * 10 }}</h1>
    <p>This is a paragraph.</p>
    <button @click="count++">Count is: {{ count }}</button>
</template>

<style scoped>
    
</style>
