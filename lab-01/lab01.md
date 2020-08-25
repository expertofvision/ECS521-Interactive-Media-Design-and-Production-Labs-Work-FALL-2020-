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

1. Copy the following script in svg.html and see the output. <br/>
    <svg height="140" width="500"> 
    <ellipse cx="200" cy="80" rx="100" ry="50" style="fill:yellow;stroke:purple;stroke-width:2" /> 
    </svg>
2. Copy the following script in svg.html and see the output. <br/>
    <svg height="250" width="500"> 
    <polygon points="220,10 300,210 170,250 123,234" style="fill:lime;stroke:purple;stroke-width:1" /> 
    </svg>
3. Copy the following script in svg.html and see the output. <br/>
    <svg height="60" width="200"> 
    <text x="0" y="15" fill="red" transform="rotate(30 20,40)">I love SVG</text> 
    </svg>

### C. To Do Questions

1. Download todo.html file.
2. Open the file in browser (chrome/firefox/ie).
3. Open the file in text editor.

#### Canvas and JavaScript

Animation
1. Examine the canvas and the definition of the ball object.
2. Replace ball.draw(); by the following code; <br/>
    function drawBall() { <br/>
      ball.x += ball.vx; <br/>
      ball.y += ball.vy; <br/>
      ball.draw() <br/>
      window.requestAnimationFrame(drawBall); <br/>
    } <br/>
   drawBall(); <br/>
 
 _Questions:_
1. Write the differences in few sentences.
2. Make the ball move only on horizontal direction.
3. Make the ball move only on vertical direction.
4. keep the ball moving inside the canvas. Hint: add an if condition to check ball.x and ball.y values.
 
 #### SVG and JavaScript
 
1. Go to SVG Editor
2. Draw a stick figure.
3. Click on <svg> button (top toolbar) and copy-paste the SVG of your drawing to the place marked in the index.html file. Save changes and refresh your browser. 

_Questions:_
1. Examine the JavaScript code below your SVG. It connects two functions to mouse-events, in relation to an SVG object called
stick_figure. Add the id attribute to <svg> tag, so that it reads id="stick_figure". Try moving the mouse over your drawing and see what happens. Write the difference in few sentences.
2. Add the properties x=0 y=0 to <svg> tag. Examine the listener keydown and the function move. Go to the browser and press the right arrow key. Check the console to see the correct key code. Do the same for the left arrow key. Replace the key codes in the move function. Move your sick figure by using the right and left arrow keys.
  

**Note:** 




