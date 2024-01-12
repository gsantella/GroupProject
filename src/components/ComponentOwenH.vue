<template>
  <div>
    <button @click="$emit('bigError')">Emit Event</button>
    <marquee>Owen</marquee>
    <h1>This is my special zone</h1>
    <p>This is a paragraph tag!</p>
    <h2>My button has been clicked {{ count }} times!</h2>
    <button @click="incrementCount">BUTTON</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    incrementCount() {
      this.count++;
    },
  },
});
</script>

<style scoped>
  marquee {
    color: darkviolet;
    font-family: "Comic Sans MS", "Comic Sans", cursive;
  }
</style>
