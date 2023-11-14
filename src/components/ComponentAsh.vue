<template>
  <div>
    <ul>
      <li v-for="i in 20" :key="i">{{ i }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numbers: Array.from({ length: 20 }, (v, k) => k + 1)
    }
  }
}
</script>