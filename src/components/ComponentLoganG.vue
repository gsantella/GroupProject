<script setup>
  function openGoogleInNewTab() {
    var googleUrl = 'https://www.google.com';

    window.open(googleUrl, '_blank');
  }
</script>

<template>
  <button onclick="openGoogleInNewTab()" class="button is-info is-rounded" >Logan</button>
</template>

<style scoped>

</style>
