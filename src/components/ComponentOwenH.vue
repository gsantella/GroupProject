<script setup>
  import {ref, defineEmits} from 'vue';
  const emit = defineEmits(['bigError']);
  const count = ref(0)
</script>

<template>
  <button @click="$emit('bigError')">Emit Event</button>
  <marquee>Owen</marquee>
  <h1>This is my special zone</h1>
  <p>This is a paragraph tag!</p>
  <h2>My button has been clicked {{ count }} times!</h2>
  <button @click="count++">BUTTON</button>
  <form action="/html/tags/html_form_tag_action.cfm" method="get">
  Star Wars Character Name:
  <input type="text" name="Star-Wars-Character" value="" maxlength="100" />
  <br />
  <input type="submit" value="Submit" />
  </form>
</template>

<style scoped>
  marquee
  {
    color:darkviolet;
    font-family: "Comic Sans MS", "Comic Sans", cursive;
  }
</style>
