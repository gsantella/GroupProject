<template>
  <div>
    <button @click="rickroll" class="rickroll-button">Click me!!</button>
  </div>
</template>

<script setup>
const rickroll = () => {
 
  window.location.href = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
};
</script>

<style scoped>
.rickroll-button {
  font-size: 1.5rem;
  padding: 10px 20px;
  background-color: #ff6f61;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.rickroll-button:hover {
  background-color: #e64a3b;
}
</style>

