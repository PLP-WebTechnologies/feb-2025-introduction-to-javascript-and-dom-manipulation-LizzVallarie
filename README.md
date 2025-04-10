# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨



















<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Dynamic DOM Example</title>
    <style>
        .box {
            padding: 20px;
            margin: 10px;
            background-color: lightblue;
        }
    </style>
</head>
<body>
    <h1 id="mainTitle">Hello World</h1>
    <p id="textContent">Click the buttons to see some magic!</p>
    
    <button onclick="changeText()">Change Text</button>
    <button onclick="changeStyle()">Change Style</button>
    <button onclick="toggleElement()">Add/Remove Box</button>
    
    <div id="container"></div>

    <script>
        // Function to change text content dynamically
        function changeText() {
            const title = document.getElementById('mainTitle');
            const paragraph = document.getElementById('textContent');
            
            title.textContent = "Text Changed!";
            paragraph.textContent = "The content has been updated dynamically!";
        }

        // Function to modify CSS styles
        function changeStyle() {
            const title = document.getElementById('mainTitle');
            const paragraph = document.getElementById('textContent');
            
            title.style.color = "blue";
            title.style 
   
.fontSize = "2.5em";
            paragraph.style.backgroundColor = "#f0f0f0";
            paragraph.style.padding = "10px";
        }

        // Function to add or remove element
        function toggleElement() {
            const container = document.getElementById('container');
            const existingBox = document.getElementById('dynamicBox');
            
            if (existingBox) {
                // If box exists, remove it
                container.removeChild(existingBox);
            } else {
                // If no box exists, create and add one
                const newBox = document.createElement('div');
                newBox.id = 'dynamicBox';
                newBox.className = 'box';
                newBox.textContent = "I'm a new box!";
                container.appendChild(newBox);
            }
        }
    </script>
</body>
</html>
