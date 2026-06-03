<!DOCTYPE html>
<html>
<head>
      <title>Calculator</title>
      <link rel="stylesheet"
</head>  
<body>    
       <div class="calculator">
            <input  type="test" id="display">
readonly>
        <div  class="buttons">
        <button
onclick="cleardisplay()">c</button> 
          <button
onclick="appendvalue('/')">/</button>
           <button
onclick="appendvalue('*')">*</button> 
            <button
onclick="deletelast()">deletebutton</button>
             <button
onclick="appendvalue('7')">7</button>
            <button
onclick="appendvalue('8')">8</button>
             <button
onclick="appendvalue('9')">9</button>
             <button
onclick="appendvalue('-')">-</button>
              
              <button
onclick="appendvalue('4')">4</button>
            <button
onclick="appendvalue('5')">5</button>
             <button
onclick="appendvalue('6')">6</button>
            <button
onclick="appendvalue('+')">+</button>
            
            <button
onclick="appendvalue('1')">1</button>
            <button
onclick="appendvalue('2')">2</button>
             <button
onclick="appendvalue('3')">3</button>
            <button
onclick="calculate()">=</button>

            <button
oneclick="appendvalue('0')">0</button>
            <button
onclick="appendvalue('.')">.</button>
       </div>
    </div>


    <script src="script.js"></script>
</body>
</html>

style.css
css

body{
    font-family:Arial, sans-serif;
    display: flex;
    justify-content: center;
    margin-top: 50px;
}
.calculator {
    width:250px;
}
#display{
    width:100%;
    height:50px;
    font-size:24px;
    text-align:right;
    margin-bottom:10px
}
.button{
    display:grid;
    grid-template-columns:repeat(4,  1fr);
    gap:5px;
}
button{
    padding:15px;
    font-size:18px
    cursor:pointer;
}

script.js

const display = 
document.getElementrybyid("display");
function appendvalue(value)  {
    display.value += value;
}
function cleardisplay() {
    display.value  = "";
}
function calculate (){
    try {
        display.value  =
eval(display.value);
    }  catch {
        display.value = "Error';
    }
}

