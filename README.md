# Ex.08 Design of a Standard Calculator
## Date:13/05/2024

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
## cal.html
```
<html >
<head>

    <title>My Calculator</title>
    <style>
        #calc {
            text-align: center;
            margin: auto;
            width: 240px;
        }
        .button {
            margin-left: 550px;
            margin-right: 550px;
            padding: 30px;
            background-color:rgb(134, 239, 42);
            color: rgb(151, 219, 151);
            border:4px solid BLACK; 
            height: 30%;
            width: 25%;
            position: absolute;
            left: 12%;
            right: 33%;
        }

        .button input[type="button"] {
            background-color:rgb(211, 172, 43);
            height: 50px;
            width: 50px;
            margin: 0 2px;
            border: 3px solid rgb(0, 0, 0);
        }
    </style>
</head>

<body style="background-color: white;">
    <h1 align="center" style="color: BLACK;">CALCULATOR</h1>
        <h3 align="center" style="color: BLACK;">praga 212222110033</h3>
        <div class="button">
            <center>
            
            <input type="text" id="t1" style="width:270px; height:30px;"><br><br>
            <input type="button" onkeydown="op(event)" onclick="f('7')" value="7">
            <input type="button" onkeydown="op(event)" onclick="f('8')" value="8">
            <input type="button" onkeydown="op(event)" onclick="f('9')" value="9">
            <input type="button" onkeydown="op(event)" onclick="f('+')" value="+">
            <input type="button" onkeydown="op(event)" value="C"  onclick="clr()"><br><br>

            <input type="button" onkeydown="op(event)" onclick="f('4')" value="4">
            <input type="button" onkeydown="op(event)" onclick="f('5')" value="5">
            <input type="button" onkeydown="op(event)" onclick="f('6')" value="6">
            <input type="button" onkeydown="op(event)" onclick="f('*')" value="x">
            <input type="button" onkeydown="op(event)" onclick="f('^0.5')" value="+/-"><br><br>
    
            <input type="button" onkeydown="op(event)" onclick="f('1')" value="1">
            <input type="button" onkeydown="op(event)" onclick="f('2')" value="2">
            <input type="button" onkeydown="op(event)" onclick="f('3')" value="3">
            <input type="button" onkeydown="op(event)" onclick="f('-')" value="-">
            <input type="button" onkeydown="op(event)" onclick="f('/')" value="%"><br><br>
        
            <input type="button" onkeydown="op(event)" onclick="f('0')" value="0">
            <input type="button" onkeydown="op(event)" onclick="f('.')"
                value=".">
            
            <input type="button" onkeydown="op(event)" onclick="f('+')" value="+">
            <input type="button" onclick="solve()" value="=" style="color: rgb(0, 0, 0); width:110px;font-weight:bolder;">
        </center>
        </div>
</body>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjs/9.4.4/math.js"></script>

<script>
    function f(val) {
        document.getElementById('t1').value += val;
    }

    function clr() {
        document.getElementById('t1').value = "";
    }

    function op(event) {
        if (event.key == '7' || event.key == '8' || event.key == '9' || event.key == '+' || event.key == '+/-' || event.key == '4' ||
            event.key == '5' || event.key == '6' || event.key == '#' || event.key == '+/-' || event.key == '1' ||
            event.key == '2' || event.key == '3' || event.key == '-' || event.key == '/' || event.key == '0' || event.key == '.') {
            document.getElementById('t1').value += event.key;
        }
    }

    var cal = document.getElementById('calc');
    cal.onkeyup = function (event) {
        if (event.keyCode == 13) {
            console.log("Enter");
            solve();
        }
    }

    function solve() {
        let x = document.getElementById('t1').value;
        let y = math.evaluate(x); // Assuming you have included the math.js library
        document.getElementById('t1').value = y;
    }
</script>

</html>
```

## OUTPUT:
![image](https://github.com/pragachellapillai/Calc/assets/148254952/b4c00013-bb33-461c-8e1d-4ea377e3a9b5)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
