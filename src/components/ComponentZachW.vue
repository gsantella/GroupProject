<script setup>
  import { ref } from 'vue'
  const count = ref(0)
  function clickMe() { 
      alert('you just took orders from a button, didnt know you stooped so low');
   }
</script>

 <template>
  <h1>Zach Willett</h1>
  <h1>AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA</h1>
    <button @click="clickMe()">press this button</button>
   ///
<button @click="count++"><h1>You clicked me {{ count }} times.</h1></button>
   ///
     <strong>satisfying right?</strong>
<p>
   <button style="background-color: red;">Stop</button>
   <button style="background-color: Yellow;">SPEED UP</button>
   <button style="background-color: green;">Go</button>
</p>
   <div>
     
   </div>
</template> 