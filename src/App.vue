<script setup>
import HelloWorld from './components/HelloWorld.vue'
  import ComponentShawn from './components/ComponentShawn.vue'
  import ComponentGuido from './components/ComponentGuido.vue'
import ComponentZachW from './components/ComponentZachW.vue'
import ComponenetNathan from './components/ComponenetNathan.vue'
import ComponentSkyler from './components/ComponentSkyler.vue'
import ComponentTravis from './components/ComponentTravis.vue'
  import ComponentLoganG from './components/ComponentLoganG.vue'
  import ComponentDevin from './components/ComponentDevin.vue'
</script>

<template>
  
  <main>

    <div class="columns">
      <div class="column" style="border:1px solid red">
        <ComponentDevin />
        <ComponentLoganG />
        <ComponentShawn />
      </div>
      <div class="column" style="border:1px solid red">
        <ComponentGuido />
        <ComponentZachW />
        <ComponentDamian />
      </div>
      <div class="column" style="border:1px solid red">
        <ComponentTravis />
        <ComponentSkyler />
        <ComponentGordon />
      </div>
    </div>    
    
  </main>
  
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
