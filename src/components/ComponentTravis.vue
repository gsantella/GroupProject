<template>
  <div>
    <button @click="openHungryVideo" class="poopoopeepee-button">Click me!!</button>
  </div>
</template>

<script setup>
const openHungryVideo = () => {
  window.open('https://www.youtube.com/watch?v=ns5NcC1iA4g&ab_channel=I%27mhungry', '_blank');
};
</script>

<style scoped>
.poopoopeepee-button {
  font-size: 1.5rem;
  padding: 10px 20px;
  background-color: #ff6f61;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.poopoopeepee-button:hover {
  background-color: #e64a3b;
}
</style>

