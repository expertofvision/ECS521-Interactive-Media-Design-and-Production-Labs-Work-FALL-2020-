<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 1
</div>


### Introduction
This lab includes basis of Canvas, SVG, Interaction and Animations.

### A. Canvas and JavaScript Examples

1. Download canvas.html file.
2. Open canvas.html file in browser (chrome/firefox/ie).
3. Open the canvas.html file in text editor.

#### Drawing in Canvas (step-by-step) with JavaScript

1. Find the canvas element. <br/>
    var canvas = document.getElementById("myCanvas");
2. Create a drawing object. <br/>
    var ctx = canvas.getContext("2d"); 
3. Draw in the canvas. <br/>
    ctx.fillStyle = "#FF0000"; <br/>
    ctx.fillRect(25, 25, 50, 50);

#### Practice Exercises

1. Draw a straight line on a canvas, use the following methods; <br/>
    moveTo(x,y) - defines the starting point of the line <br/>
    lineTo(x,y) - defines the ending point of the line <br/>
   To actually draw the line, you must use one of the "ink" methods, like stroke().
2. draw a circle on a canvas, use the following methods: 

beginPath() - begins a path 

arc(x,y,r,startangle,endangle) - creates an arc/curve. To create a circle with arc(): Set start angle to 0 and end angle to 2*Math.PI. The x and y parameters define the x- and y-coordinates of the center of the circle. The r parameter defines the radius of the circle. 

Define a circle with the arc() method. Then use the stroke() method to actually draw the circle.
