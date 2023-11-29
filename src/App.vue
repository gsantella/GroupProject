<script setup>
import HelloWorld from './components/HelloWorld.vue'
  import ComponentAsh from './components/ComponentAsh.vue'
  import ComponentZachS from './components/ComponentZachS.vue'
  import ComponentShawn from './components/ComponentShawn.vue'
  import ComponentGuido from './components/ComponentGuido.vue'
import ComponentZachW from './components/ComponentZachW.vue'
import ComponenetNathan from './components/ComponenetNathan.vue'
import ComponentSkyler from './components/ComponentSkyler.vue'
import ComponentTravis from './components/ComponentTravis.vue'
  import ComponentLoganG from './components/ComponentLoganG.vue'
  import ComponentDevin from './components/ComponentDevin.vue'
  import ComponentGordon from './components/ComponentGordon.vue'
  import ComponentDan from './components/ComponentDan.vue'
  import ComponentDamian from './components/ComponentDamian.vue'
  import ComponentLoganW from './components/ComponentLoganW.vue'
  import ComponentAdam from './components/ComponentAdam.vue'
  import ComponentBen from './components/ComponentBen.vue'
  import ComponentOwenH from './components/ComponentOwenH.vue'
  import ComponentMarcus from './components/ComponentMarcus.vue'
</script>

<template>
  
  <main>

    <div class="columns">
      <div class="column" style="border:1px solid red">
        <div class="card">
          <div class="card-content">  
            <ComponentBen />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentAdam />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentOwenH />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentMarcus />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentAsh />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentZachS />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentGordon />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentDevin />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentLoganG />
          </div>
        </div>
        <div class="card">
          <div class="card-content">  
            <ComponentShawn />
          </div>
        </div>
      </div>
      <div class="column" style="border:1px solid red">
        <div class="card">
          <div class="card-content"> 
            <ComponentGuido />
          </div>
        </div>
        <div class="card">
          <div class="card-content"> 
            <ComponentZachW />
          </div>
        </div>
        <div class="card">
          <div class="card-content"> 
            <ComponentDamian />
          </div>
        </div>  
      </div>
      <div class="column" style="border:1px solid red">
        <div class="card">
          <div class="card-content">  
            <ComponentDan />
          </div>
        </div>
        <div class="card">
          <div class="card-content"> 
            <ComponentTravis />
          </div>
        </div>          
        <div class="card">
          <div class="card-content"> 
            <ComponentSkyler />
          </div>
        </div>            
        <div class="card">
          <div class="card-content"> 
            <ComponentGordon />
          </div>
        </div>  
        <div class="card">
          <div class="card-content"> 
            <ComponentLoganW />
          </div>
        </div>  
        <div class="card">
          <div class="card-content"> 
            <ComponenetNathan />
          </div>
        </div>  

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
