<!DOCTYPE html>
<html>
<head>
    <meta charset = UTF-8>
    <title>Assessment Exercise Chapter 6 - Petrol Calculator</title>
    <style @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

body {
   margin: 0;
   padding: 0;
   overflow: hidden; 
   background-color: white;
   font-family: "Poppins", sans-serif;
   color: black
}

/* Styles header to resemble that of a gas station's roof lining */
header {

    display: flex;
    background-color: rgb(255, 57, 57);
    border-bottom: 5px solid rgb(151, 36, 36);
    color: white
}

/* Adds space between title and edge of webpage */
h1 {

    margin-left: 15px

}

/* Centres webpage's main content */
main {

    justify-content: center;
    align-items: center;    
    text-align: center;     

}

/* Adds padding between sections of content */
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

/* Makes the calculate button transition colour to green  when a cursor hover over them  */
.calculateButton:hover {

    background-color: darkgreen;
    color: white;
    border: 2px solid black;
    border-radius: 10px;
    transition: background-color 1s

}

/* Stylesheet for all buttons */
button {

    border: 2px solid black;
    border-radius: 10px

}

/* Makes the reset Button transition colour to red when a cursor hover over them  */
.resetButton:hover {

    background-color: darkred;
    color: white;
    border: 2px solid black;
    border-radius: 10px;
    transition: background-color 1s

}> <!--Link to stylesheet -->
    <script src = "exercise6_javascript.js"></script> <!--Link to javascript file -->
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
