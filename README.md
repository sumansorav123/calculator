<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculater</title>
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    body {
        background-color: rgb(219, 251, 255);
    }

    .calculator-container {
        width: 400px;
        height: 75%;
        border: 2px solid rgb(255, 0, 0);
        position: absolute;
        left: 33em;
        top: 7em;
        background-color: rgb(35, 35, 35);
        color: aliceblue;
        box-shadow: 0 0 25px rgb(223, 0, 0);
        border-radius: 12px;
    }

    .calculator-container h1 {
        text-align: center;
    }

    .display-value {
        height: 60px;
        margin: 10px;
        border: 1px solid skyblue;
        border-radius: 10px;
        width: 93%;
    }

    .display-value input {
        position: absolute;
        left: 12px;
        top: 48px;
        width: 357px;
        height: 44px;
        background-color: aliceblue;
        padding: 5px;
        border-radius: inherit;
        font-size: 34px;
    }

    .calculator-buttons {
        display: flex;
        align-content: space-between;
        justify-content: space-between;
        align-items: center;
        flex-direction: column;
        position: absolute;
        left: 24px;
    }

    .calculator-btn1 {
        display: flex;
        flex-direction: row;
        left: 7px
    }

    .calculator-btn1 button {
        display: flex;
        justify-content: space-between;
        align-items: center;
        align-content: space-between;
        width: 60px;
        height: 42px;
        justify-content: center;
        border: 5px solid;
        border-radius: 50%;
        margin: 13px;
        background-color: rgb(88, 55, 0);
        color: #ffffff;
        cursor: pointer;
    }

    .calculator-btn1 button:hover {
        background-color: rgb(202, 108, 0);
        color: azure;
        cursor: pointer;
        font-size: 23px;
        transform: 0.9s;
    }

    .calculator-btn2 {
        display: flex;
        flex-direction: column;
        position: absolute;
        right: 0px;
        top: 102%;
        left: 268px;
    }

    .calculator-btn2 button {
        display: flex;
        justify-content: space-between;
        align-items: center;
        align-content: space-between;
        width: 60px;
        height: 42px;
        justify-content: center;
        border: 5px solid;
        border-radius: 50%;
        margin: 13px;
        background-color: rgb(183, 86, 2);
        color: aliceblue;
        cursor: pointer;
    }

    .calculator-btn2 button:hover {
        background-color: black;
        cursor: pointer;
        font-size: 25px;
        transform: 0.9s;
    }

    .calculator-btn3 {
        display: flex;
        flex-direction: row;
        position: absolute;
        right: 76px;
        top: 102%;
        flex-wrap: wrap;

    }

    .calculator-btn3 button {
        display: flex;
        background-color: rgb(20, 13, 0);
        justify-content: space-between;
        align-items: center;
        align-content: space-between;
        width: 60px;
        height: 42px;
        justify-content: center;
        border: 5px solid;
        border-radius: 50%;
        margin: 13px;
        cursor: pointer;
        color: aliceblue;
        font-size: 15px;
    }

    .calculator-btn3 button:hover {
        background-color: rgb(194, 95, 2);
        font-size: 25px;
        transform: 0.9s;
    }
</style>

<body>
    <div class="calculator-container">
        <h1>calculator</h1>
        <div class="calculator-display">
            <div class="display-value">
                <input type="text" id="display-Output" placeholder="0">
            </div>
            <div class="calculator-buttons">
                <div class="calculator-btn1">
                    <button onclick="Clear()">AC</button>
                    <button onclick="del( )">DEL</button>
                    <button onclick="display('/')">/</button>
                    <button onclick="display('*')">*</button>
                </div>

                <div class="calculator-btn2">
                    <button onclick="display('-')">-</button>
                    <button onclick="display('+')">+</button>
                    <button onclick="Calculate('=')" class="equal">=</button>
                    <button onclick="display('%')">%</button>
                </div>

                <div class="calculator-btn3">
                    <button onclick="display('1')">1</button>
                    <button onclick="display('2')">2</button>
                    <button onclick="display('3')">3</button>
                    <button onclick="display('4')">4</button>
                    <button onclick="display('5')">5</button>
                    <button onclick="display('6')">6</button>
                    <button onclick="display('7')">7</button>
                    <button onclick="display('8')">8</button>
                    <button onclick="display('9')">9</button>
                    <button onclick="display('0')">0</button>
                    <button onclick="display('00')">00</button>
                    <button onclick="display('.')">.</button>
                </div>
            </div>
</body>
<script>
    let displayOutput = document.getElementById("display-Output");
    function display(num) {
        displayOutput.value += num;
    }
    function Calculate() {
        let displayValue = displayOutput.value;
        if (displayValue.length > 1) {
            displayOutput.value = eval(displayValue);
        }
    }
    function Clear() {
        displayOutput.value = "";
    }
    function del() {
        displayOutput.value = displayOutput.value.slice(0, -1);
    }    
</script>

</html>
