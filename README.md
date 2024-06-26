3555# Intorduction to Javascript and Interactive Charts and Graphs

## Description:
In this week, you will explore the fundamentals of JavaScript, focusing on variables, data types, functions, and manipulating the Document Object Model (DOM). Additionally, you will implement interactive charts and graphsn using Chart.js. This assignment will provide hands-on experience with JavaScript programming and data visualization techniques.

## Requirements:

### JavaScript Fundamentals:
        Create an HTML file named index.html.
        Include a <script> tag to link an external JavaScript file named script.js.
        Implement JavaScript code to cover the following concepts:
            Declare variables of different data types (string, number, boolean).
            Define and call functions to perform simple operations; name them as follows:
            add
            subtract
            divide
            multiply.
            Use console.log() to print output and debug code.
index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Introduction to JavaScript and Interactive Charts</title>
    <!-- Link Chart.js library -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Link external JavaScript file -->
    <script src="script.js" defer></script>
    <style>
        /* Optional: Add some basic styling */
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        canvas {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Introduction to JavaScript and Interactive Charts</h1>

    <!-- Example of DOM elements for user interaction -->
    <div>
        <label for="num1">Enter Number 1:</label>
        <input type="number" id="num1" name="num1">
        <br>
        <label for="num2">Enter Number 2:</label>
        <input type="number" id="num2" name="num2">
        <br>
        <button onclick="calculate()">Calculate</button>
        <p id="result"></p>
    </div>

    <!-- Canvas element for Chart.js -->
    <div>
        <canvas id="myChart" width="400" height="400"></canvas>
    </div>
</body>
</html>


script.js

// Declare variables of different data types
var name = "John Doe";
var age = 30;
var isStudent = true;

// Define and call functions to perform simple operations
function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

function divide(a, b) {
    if (b === 0) {
        console.error("Cannot divide by zero!");
        return null;
    }
    return a / b;
}

function multiply(a, b) {
    return a * b;
}

// Function to perform operations and update the result
function performOperation(operation) {
    var num1 = parseFloat(document.getElementById("num1").value);
    var num2 = parseFloat(document.getElementById("num2").value);
    var result;

    switch (operation) {
        case 'add':
            result = add(num1, num2);
            break;
        case 'subtract':
            result = subtract(num1, num2);
            break;
        case 'divide':
            result = divide(num1, num2);
            break;
        case 'multiply':
            result = multiply(num1, num2);
            break;
        default:
            result = "Unknown operation";
    }

    document.getElementById("result").textContent = "Result: " + result;
    console.log("Result: " + result);
}

// Interactive Charts and Graphs with Chart.js
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    }
});
eractions (e.g., click events, input events).
        Ensure that your DOM manipulation code enhances the interactivity and usability of the web page.

        
### DOM Manipulation:
        Expand your index.html file to include elements for user interaction (e.g., buttons, input fields).
        Use JavaScript to manipulate the DOM in response to user actions. For example, update text content, change styles, or show/hide elements based on user input.
        Implement event listeners to handle user int// JavaScript Fundamentals

Explanation
HTML Structure:

Added more user interaction elements, including an extra button and a hidden message.
calculateButton: Triggers the calculate() function to perform an addition and display the result.
toggleButton: Toggles the visibility of the hidden message using the toggleHiddenMessage() function.
JavaScript (script.js):

Event Listeners: Added event listeners to handle button clicks, which call the corresponding functions (calculate and toggleHiddenMessage).
DOM Manipulation:
calculate(): Fetches input values, performs an addition, and updates the result text and its color based on the calculated value.
toggleHiddenMessage(): Toggles the display property of the hidden message to show or hide it.
Chart.js Integration: Same as before, initializes a bar chart using Chart.js.

Testing
Open index.html in a Web Browser: Open the file in a browser to see the web page.
Check User Interaction:
Enter values in the input fields and click the "Calculate" button to see the result.
Click the "Toggle Hidden Message" button to show or hide the hidden message.
View Console Output: Open the browser's developer console (Ctrl+Shift+J or Cmd+Option+J) to see the logged messages and any debugging information.
Submission
GitHub Repository: After verifying the functionality, push the files (index.html and script.js) to a GitHub repository.
Submission Link: Share the link to your GitHub repository for evaluation.
This setup ensures that you meet the assignment requirements by demonstrating JavaScript fundamentals, DOM manipulation, and integration of interactive charts using Chart.js. Adjust the content and styling as needed to fit the assignment's criteria and your design preferences.




### Interactive Charts and Graphs:
        Integrate the Chart.js library into your project by adding the necessary <script> tag to your HTML file.
        Create a canvas element in your HTML file to render the chart.

  ### Submission:
        Submit the link to your GitHub repository for evaluation, through the github classroom.



        
