<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 1
</div>


### About this Lab
This lab includes basis of Canvas, SVG, Interaction and Animations.

### A. Canvas and JavaScript

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

#### Practice Examples

1. Draw a straight line on a canvas, use the following methods; <br/>
    moveTo(x,y) - defines the starting point of the line <br/>
    lineTo(x,y) - defines the ending point of the line <br/>
   To actually draw the line, you must use one of the "ink" methods, like stroke().
2. Draw a circle on a canvas, use the following methods; <br/>
    beginPath() - begins a path <br/>
    arc(x,y,r,startangle,endangle) - creates an arc/curve. To create a circle with arc(): Set start angle to 0 and end angle to 2*Math.PI. The x and y parameters     define the x- and y-coordinates of the center of the circle. The r parameter defines the radius of the circle. <br/>
   Define a circle with the arc() method. Then use the stroke() method to actually draw the circle.
3. Draw text on a canvas, the most important property and methods are; <br/>
    font - defines the font properties for the text <br/>
    fillText(text,x,y) - draws "filled" text on the canvas <br/>
    strokeText(text,x,y) - draws text on the canvas (no fill) <br/>
4. Draw an image on a canvas, use the following method; <br/>
    drawImage(image,x,y) <br/>
   You need to first define image as follows; <br/>
    <img id="scream" width="220" height="277" src="pic_the_scream.jpg" alt="The Scream"> <br/>
   Then, var img = document.getElementById("scream"); will be used. <br/>
   Draw Paths on canvas like this using following script; <br/>
    ctx.beginPath();                
    ctx.arc(75,75,50,0,Math.PI*2,true);  // Outer circle                               

    ctx.moveTo(110,75);               
    ctx.arc(75,75,35,0,Math.PI,false);   // Mouth                               

    ctx.moveTo(65,65);               
    ctx.arc(60,65,5,0,Math.PI*2,true);  // Left eye                               

    ctx.moveTo(95,65);                
    ctx.arc(90,65,5,0,Math.PI*2,true);  // Right eye               
    
    ctx.stroke();

### B. SVG and JavaScript

1. Download svg.html file.
2. Open svg.html in browser (chrome/firefox/ie).
3. Open svg.html in text editor.

#### Practice Examples

1. Copy the following script in svg.html and see the output.
    <svg height="140" width="500"> 
    <ellipse cx="200" cy="80" rx="100" ry="50" style="fill:yellow;stroke:purple;stroke-width:2" /> 
    </svg>
2. Copy the following script in svg.html and see the output.
    <svg height="250" width="500"> 
    <polygon points="220,10 300,210 170,250 123,234" style="fill:lime;stroke:purple;stroke-width:1" /> 
    </svg>
3. Copy the following script in svg.html and see the output.
    <svg height="60" width="200"> 
    <text x="0" y="15" fill="red" transform="rotate(30 20,40)">I love SVG</text> 
    </svg>

