<script setup>
  
  function appendToDisplay(value) {
      document.getElementById('display').value += value;
  }

  function calculate() {
      try {
          document.getElementById('display').value = eval(document.getElementById('display').value);
      } catch (error) {
          document.getElementById('display').value = 'Error';
      }
  }

  function clearDisplay() {
      document.getElementById('display').value = '';
  }

</script>
 

<template>

  <div id="calculator">
      <input type="text" id="display" readonly>
      <br>
      <input type="button" value="7" onclick="appendToDisplay('7')">
      <input type="button" value="8" onclick="appendToDisplay('8')">
      <input type="button" value="9" onclick="appendToDisplay('9')">
      <input type="button" value="/" onclick="appendToDisplay('/')">
      <br>
      <input type="button" value="4" onclick="appendToDisplay('4')">
      <input type="button" value="5" onclick="appendToDisplay('5')">
      <input type="button" value="6" onclick="appendToDisplay('6')">
      <input type="button" value="-" onclick="appendToDisplay('-')">
      <br>
      <input type="button" value="1" onclick="appendToDisplay('1')">
      <input type="button" value="2" onclick="appendToDisplay('2')">
      <input type="button" value="3" onclick="appendToDisplay('3')">
      <input type="button" value="+" onclick="appendToDisplay('+')">
      <br>
      <input type="button" value="0" onclick="appendToDisplay('0')">
      <input type="button" value="." onclick="appendToDisplay('.')">
      <input type="button" value="=" onclick="calculate()">
      <input type="button" value="C" onclick="clearDisplay()">
  </div>


 
</template>

<style scoped>
  input[type="text"] {
      width: 100%;
      padding: 10px;
      margin: 5px 0;
      display: inline-block;
      border: 1px solid #ccc;
      box-sizing: border-box;
  }
  input[type="button"] {
      width: 40px;
      height: 40px;
      font-size: 18px;
      margin: 5px;
  }
  #calculator {
      width: 350px;
      margin: 10px auto;
      border: 1px solid #ccc;
      padding: 10px;
      border-radius: 5px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
</style>