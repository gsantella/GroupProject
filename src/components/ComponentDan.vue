<script>
  let count = 0
  function increment() {
    document.getElementById("clicker").innerHTML = "You shouldn't have clicked me " + count + " times >:o" ;
    count--;
  }
  export default {
    data() {
      return {
        alignLeft: false
      };
    },
    methods: {
      toggleAlignment() {
        this.alignLeft = !this.alignLeft;
      }
    }
  };
</script>
<template>
  <div>
    <h1><marquee>This is Daniel's button no touch</marquee></h1>
    <button id="clicker" @click="increment()">Not A Button!! >:(</button>
    <button @click="toggleAlignment" :style="{ float: alignLeft ? 'left' : 'none' }">Click me</button>
  </div>
</template>
<style scoped>
h1 {
  color: darkblue;
}
button {
  align: center;
}
</style>


