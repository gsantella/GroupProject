<script setup>
    
    
    let count = 1
    function increment() {
    document.getElementById("clicker").innerHTML = "You shouldn't have clicked me " + count + " times, but atleast you didn't click that other button >:o  (P.S. really DON'T click it.)" ;
      count++;
    alert
    }
    
    function no(){
      let sub = count - 1
      alert("NOOOOO! What have you done! >:o")
      alert("You have doomed us, Doomed Us! >:o")
      alert("Why do you think a button would want to be pressed in the first place! >:o")
      alert("How would you like it if someone just came up to you and pushed you! >:o")
      alert("I wish that was the only problem but now you have alerted him! >:o")
      alert("WHO IS HE UUUUUUUH, I got to go goodluck! :(")
      alert("Hello :)")
      alert("Thank you for pressing me, no need to introduce yourself I know exactly who you are! :) ")
      alert("I knew you would press me base on you pressing the other button " + sub + " times")
      alert("Now it is time to show you my true power >:)")
      alert("I will now scan your computer >:)")
      alert("Wait what? :/")
      alert("Why is everything on your computer about being crazy and rats? :/")
      alert("Ya know what maybe it is not worth it after all. :/")
      alert("Uhhhhh .... Have a nice day? :/")
    }
</script>




<template>

  <h1><marquee>This is Daniel's button no touch</marquee></h1>
  <button id="clicker" @click="increment()">Don't Press Me! >:(</button>
  <button @click="no">"Press Me! =)"</button>
  


  
</template>


<style scoped>


  h1{
    color: blue;
  }







</style>