<script setup>
let buttoncount = 0;
let dontclick = "Don't click me 6 times :) ";
function hi(){
  alert("hi")
}
function guidoButton(){
  buttoncount ++
  
  if (buttoncount < 7){
    document.getElementById("add_message").innerHTML = '<marquee behavior="scroll" direction="up" scrollamount="1">GUIDO</marquee>'+ '<marquee behavior="scroll" direction="left" scrollamount="5">GUIDO</marquee>'+ dontclick +buttoncount;}
    if (buttoncount ==  6){
      setTimeout(() => {yellow();}, 3300);
    }
    

     if (buttoncount == 1 ){
      dontclick = "You are making a mistake ";
      
      return
    }
      
    else if (buttoncount == 2){
      dontclick = "you are making a huge mistake ";
      return
    }
    else if (buttoncount == 3){
      dontclick = "do you not realize the consequences?? ";
      
      return
    }
    else if (buttoncount == 4){
    dontclick = "you are MAD?? MAD WITH POWER!!??! ";
      
      return

    }
    else if (buttoncount == 5){
    dontclick = "You brought this on yourself. ";
    }
    }
    
  function yellow(){
    document.write("<h1><marquee behavior='scroll' scrollamount='25'>Guido, a man of distinct character and individuality, found himself at a crossroads one day, contemplating a seemingly mundane yet significant decision – whether or not to shave. As the morning sunlight streamed through his window, casting a warm glow on his reflection, Guido stood before the mirror, pondering the transformative power of a razor. Guido's facial hair had become a distinctive feature, a testament to his journey and experiences. Each strand seemed to tell a story, a visual timeline of moments, laughter, and challenges. However, as he gazed into the mirror, a sense of curiosity and the desire for change lingered in his mind.The decision to shave was not merely a superficial one; it carried the weight of symbolism and self-discovery. Guido, known for his adventurous spirit and openness to new experiences, saw this act as a chance to embrace transformation and invite a fresh perspective into his life. Shaving, in Guido's eyes, wasn't about conforming to societal standards or adhering to external expectations. It was a personal choice, an intentional step towards self-renewal. As the razor glided across his face, Guido felt a sense of liberation, as if shedding the old to make way for the new. The familiar contours of his face re-emerged, revealing features that had long been hidden beneath the beard. Guido couldn't help but smile at the newfound lightness, both physically and metaphorically. The act of shaving became a ritual of self-care, a deliberate investment in his well-being. In the days that followed, Guido noticed subtle shifts in his perspective and interactions. Stripped of the facial hair that had become a part of his identity, he felt a renewed connection with his own reflection. It was as if the act of shaving had unveiled a truer version of himself, unburdened by the external layers that had accumulated over time. As Guido navigated through life with his clean-shaven look, he discovered the power of embracing change and the beauty that comes with letting go. The decision to shave, once a seemingly simple choice, had become a catalyst for personal growth and self-discovery. In the end, Guido realized that the journey of self-exploration is ongoing, and sometimes, a small, seemingly routine decision like shaving can be a profound expression of one's autonomy and the pursuit of authenticity. </marquee></h1>")
    let count = 0;
    while (count != 100){
      if (count % 2 != 0){
        document.write("<marquee scrollamount ='70'>BUCKETS</marquee> <style scoped> marquee{background-color: yellow;} </style><script>");}
        
      else{
        document.write('<marquee><button>"ICECREAM PICKERRRRRRRRRRR"</button></marquee><marquee behavior="scroll" direction = "down"><button>guido</button></marquee> <style scoped> marquee{background-color: yellow;} button{color: purple; background-color: white}</style>');}
  
      
      count ++;
      

      }
  }
</script>
<script>
  import { ref } from 'vue';

  export default {
    setup() {
      const buttonX = ref(0);
      const buttonY = ref(0);

      const moveButton = () => {
        const newX = Math.floor(Math.random() * window.innerWidth);
        const newY = Math.floor(Math.random() * window.innerHeight);

        buttonX.value = newX;
        buttonY.value = newY;
      };

      return {
        buttonX,
        buttonY,
        moveButton,
      };
    },
  };
  </script>



<template>
    <div id="movableElement"
      :style="{ left: `${elementX}px`, top: `${elementY}px` }"></div>
  <button id ="add_message" @click="guidoButton">Bucket</button>
    <!--<button id="movableButton"
        @click="moveButton"
      :style="{ transform: `translate(${buttonX}px, ${buttonY}px)` }"
      >move me</button>-->
</template>

<style scoped>
button{
  background-color: pink;
  text-align: center;
  border-width: 17px;
  width: 190px;
}
#movableButton {
    position: absolute;
    transition: all 0.5s ease-in-out;
  }/* Add smooth transition effect */
  
</style>