  <template>
  <div>
    <button @click="startDVD">Play</button>
    <div id="dvdLogo" v-show="isMoving" style="position: absolute; top: {{ dvdTop }}px; left: {{ dvdLeft }}px;">
      <img src="dvd_logo.png" alt="DVD Logo" width="100" height="50">
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isMoving = ref(false);
let dvdTop = 0;
let dvdLeft = 0;
let speedX = 3;
let speedY = 3;

function startDVD() {
  isMoving.value = true;

  const screenWidth = window.innerWidth - 100;
  const screenHeight = window.innerHeight - 50;

  const moveDVD = () => {
    dvdTop += speedY;
    dvdLeft += speedX;

    if (dvdTop >= screenHeight || dvdTop <= 0) {
      speedY *= -1;
    }
    if (dvdLeft >= screenWidth || dvdLeft <= 0) {
      speedX *= -1;
    }

    if (isMoving.value) {
      requestAnimationFrame(moveDVD);
    }
  };

  moveDVD();
}

</script>

<style scoped>
button {
  margin-bottom: 20px;
}
</style>