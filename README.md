# caclulator
#HTML
<!DOCTYPE html>
<html lang="en">
<head>

    <title>calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
<main id="main">

    <input type="text"  id="display" readonly>


    <div id="button-con">

        <button onclick="screenClear()">AC</button>
        <button onclick="getInput('1')">1</button>
        <button onclick="getInput('2')">2</button>
        <button onclick="getInput('+')">+</button>
        <button onclick="getInput('3')">3</button>
        <button onclick="getInput('4')">4</button>
        <button onclick="getInput('-')">-</button>
        <button onclick="getInput('5')">5</button>
        <button onclick="getInput('6')">6</button>
        <button onclick="getInput('*')">x</button>
        <button onclick="getInput('7')">7</button>
        <button onclick="getInput('8')">8</button>
        <button onclick="getInput('/')">/</button>
        <button onclick="getInput('9')">9</button>
        <button onclick="getInput('%')">%</button>
        <button onclick="getInput('.')">.</button>
        <button onclick="getInput('0')">0</button>
        <button onclick="resultShow()">=</button>

    </div>


</main>

<script src="javascript.js"></script>
</body>
</html>


#JAVA SCRIPT
let input='';
function getInput(x)
{
    input=input+x;
    document.getElementById('display').value=input;
}

function screenClear()
{
    input='';
    
    document.getElementById('display').value=input;
}

function resultShow(){

let result=eval(input);
input=result;
document.getElementById('display').value=input;
}

#CSS

body{
    background-color: dimgrey;
}
#main{

    margin: 40px 550px;

border:1px black solid;
height: 500px;
width: 300px;
border-radius: 5px;
background-color: cadetblue;
}

/* button section */
#button-con{
display: flex;
flex-wrap: wrap;
margin-left: 12px;

}
button{
    height: 55px;
    width:75px;
    margin: 7px;
    border: 2px black solid;
    border-radius: 5px;
    font-size: 30px;
    font-weight: 700;
    background-color: blanchedalmond;
    
}

button:active{
    background-color: greenyellow;
    height: 50px;
    width:70px;
    margin: 8px;

}



#display{
    border: 2px black solid;
    border-radius: 5px;
    height: 50px;
    width: 270px;
    margin: 12px;
    font-size: 26px;
    font-weight: 700;
}
