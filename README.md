<!DOCTYPE html>
<html>
<head>
    <meta charset = UTF-8>
    <title>Assessment Exercise Chapter 6 - Petrol Calculator</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
        body {
           margin: 0;
           padding: 0;
           overflow: hidden; 
           background-color: white;
           font-family: "Poppins", sans-serif;
           color: black
        }
        header {
            display: flex;
            background-color: rgb(255, 57, 57);
            border-bottom: 5px solid rgb(151, 36, 36);
            color: white
        }
        h1 {
            margin-left: 15px
        }
        main {
            justify-content: center;
            align-items: center;    
            text-align: center;     
        }
        .group_1 {
            padding-bottom: 10px
        }
        .group_2 {
            padding-top: 10px;
            padding-bottom: 10px
        }
        .group_3 {
            padding-top: 10px
        }
        .calculateButton:hover {
            background-color: darkgreen;
            color: white;
            border: 2px solid black;
            border-radius: 10px;
            transition: background-color 1s
        }
        button {
            border: 2px solid black;
            border-radius: 10px
        }
        .resetButton:hover {
            background-color: darkred;
            color: white;
            border: 2px solid black;
            border-radius: 10px;
            transition: background-color 1s
        }
    </style>
    <script>
        function calculateTotal () {
        let c = Number(document.getElementById("cost").value); // Cost of petrol per litre, default 1.72
        let n = Number(document.getElementById("number").value); // Number of litres purchased
        let total = c * n; 
        document.getElementById("total").innerText = total
        }
        function resetCost () {
        document.getElementById("total").innerText = "0";
        }
    </script>
</head>
<body>
    <header>
        <h1>Petrol Calculator Webpage</h1>
    </header>
    <main> 
        <div class = "group_1">
            <h3>Cost of petrol per litre</h3>
            <input type = 'number' value = "1.72" id = "cost"> <!-- Cost of petrol per litre -->
        </div>
        <div class = "group_2">
            <h3>Number of litres purchased</h3>
            <input type = 'number' id = "number"> <!-- Number of litres purchased -->
        </div>
        <div class = "group_3">
        <button class = "calculateButton" onclick = "calculateTotal()">Calculate Total</button> <!-- Activate calculation function -->
        <button class = "resetButton" onclick = "resetCost()">Reset</button> <!-- Resets total cost -->
        <p>Total Cost: <span id = "total">0</span></p> <!-- Displays total cost after pressing calculate total button -->
        </div>
    </main>
</body>
</html>
