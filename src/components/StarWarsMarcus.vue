<script setup>
    import { ref, defineProps } from 'vue';

    const props = defineProps({id: {type: Number, required: true}})

    const person = ref({})

    fetch(`https://swapi.dev/api/people/${props.id}`)
        .then((response) => {
            return response.json()
        })
        .then((object) => {
            person.value = object
        })

</script>

<template>
    <h1>Star Wars Marcus</h1>
    <div v-if="!person.detail">
        <h2 v-if="person.name">{{ person.name }}</h2>
        <h3 v-if="person.mass">{{ person.mass }} kg</h3>
    </div>
    <h2 v-else>Character Not Found</h2>
</template>

<style scoped>
    h1 {
        font-weight: bold;
        font-size: 2rem;
    }

    h2 {
        font-weight: bold;
        font-size: 1.5rem;
    }
</style>