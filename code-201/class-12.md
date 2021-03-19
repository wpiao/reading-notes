# Read: 12 - Chart.js, Canvas 

Chart.js is a popular JS library to easily create stunning animated charts. It is far better for displaying data visually than tables.

## Setting up / Installation  
There are two ways to use Chart.js. 
1. Download Chart.min.js and then import the script
  ```html
  <head>
    <script src="Chart.min.js"></script>
  </head>
  ```
2. Install Chart.js library through terminal  
  Terminal command: `npm i chart.js --save`

## Use cases  
1. Drawing a line chart
  ```html
  <!-- First, create a canvas element -->
  <canvas id="buyers" width="600" height="400"></canvas>
  ```
  ```javascript
  // Get the canvas element
  let buyers = document.getElementById('buyers').getContext('2d');
  // Instantiate a new line chart and pass buyerData
  new Chart(buyers).Line(buyerData);

  // create a buyerData object. The object has to follow below format.
  let buyerData = {
    labels : ["January","February","March","April","May","June"],
    datasets : [
      {
        fillColor : "rgba(172,194,132,0.4)",
        strokeColor : "#ACC26D",
        pointColor : "#fff",
        pointStrokeColor : "#9DB86D",
        data : [203,156,99,251,305,247]
      }
    ]
  }
  ```