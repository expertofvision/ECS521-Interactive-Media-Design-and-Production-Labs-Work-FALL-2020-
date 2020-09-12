<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 1
</div>


### About this Lab
This lab includes basis of Canvas, SVG, Interaction and Animations.

### A. Canvas and JavaScript

1. Download [canvas.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-01/canvas.html) file.
2. Open canvas.html file in browser (chrome/firefox/ie).
3. Open the canvas.html file in text editor.

#### Drawing in Canvas (step-by-step) with JavaScript
Tip: The below source code will be inserted between "<script></script>" element. We will be studying JavaScript in next lecture.

1. Find the canvas element. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var canvas = document.getElementById("myCanvas");
2. Create a drawing object. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var ctx = canvas.getContext("2d"); 
3. Draw in the canvas. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.fillStyle = "#FF0000"; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.fillRect(25, 25, 50, 50);

#### Practice Examples

1. Draw a [straight line](https://www.w3schools.com/graphics/canvas_coordinates.asp) on a canvas, use the following methods; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; moveTo(x,y) - defines the starting point of the line <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; lineTo(x,y) - defines the ending point of the line <br/>
   To actually draw the line, you must use one of the "ink" methods, like stroke().
2. Draw a [circle](https://www.w3schools.com/graphics/canvas_coordinates.asp) on a canvas, use the following methods; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; beginPath() - begins a path <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; arc(x,y,r,startangle,endangle) - creates an arc/curve. To create a circle with arc(): Set start angle to 0 and end angle     to 2*Math.PI. The &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x and y parameters     define the x- and y-coordinates of the center of the circle. The r parameter defines the radius of the circle. <br/>
   Define a circle with the arc() method. Then use the stroke() method to actually draw the circle.
3. Draw [text](https://www.w3schools.com/graphics/canvas_text.asp) on a canvas, the most important property and methods are; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; font - defines the font properties for the text <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fillText(text,x,y) - draws "filled" text on the canvas <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; strokeText(text,x,y) - draws text on the canvas (no fill) <br/>
4. Draw an [image](https://www.w3schools.com/graphics/canvas_images.asp) on a canvas as follows; <br/>
   Download [pic_the_scream.jpg](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-01/pic_the_scream.jpg) and define in the script using html. Remember to fix image width and height. <br/>
   Then, var img = document.getElementById("scream"); will be used. <br/>
5. Draw Paths on canvas like this using following script and see the output; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.beginPath();                
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.arc(75,75,50,0,Math.PI*2,true);  // Outer circle                               

    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.moveTo(110,75);               
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.arc(75,75,35,0,Math.PI,false);   // Mouth                               

    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.moveTo(65,65);               
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.arc(60,65,5,0,Math.PI*2,true);  // Left eye                               

    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.moveTo(95,65);                
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.arc(90,65,5,0,Math.PI*2,true);  // Right eye               
    
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.stroke();

### B. SVG and JavaScript

1. Download [svg.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-01/svg.html) file.
2. Open svg.html in browser (chrome/firefox/ie).
3. Open svg.html in text editor.

#### Practice Examples

1. Draw Ellipse using following [link](https://www.w3schools.com/graphics/svg_ellipse.asp) in svg.html.
2. Draw Polygon using following [link](https://www.w3schools.com/graphics/svg_polygon.asp) in svg.html.
3. Write a text using following [link](https://www.w3schools.com/graphics/svg_text.asp) in svg.html.

### C. To Do Questions

1. Download [todo.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-01/todo.html) file.
2. Open the file in browser (chrome/firefox/ie).
3. Open the file in text editor.

#### Canvas and JavaScript

Animation
1. Examine the canvas and the definition of the ball object.
2. Replace ball.draw(); by the following code; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; function drawBall() { <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ball.x += ball.vx; <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ball.y += ball.vy; <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ball.draw() <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; window.requestAnimationFrame(drawBall); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; drawBall(); <br/>
 
 _Questions:_
1. Make the ball move only on horizontal direction.
2. Make the ball move only on vertical direction.
3. keep the ball moving inside the canvas. Hint: add an if condition to check ball.x and ball.y values.
 
 #### SVG and JavaScript
 
1. Go to [SVG Editor](https://svg-edit.github.io/svgedit/src/editor/svg-editor.html).
2. Draw a stick figure.
3. Click on <svg> button (top toolbar) and copy-paste the SVG of your drawing to the place marked in the index.html file. Save changes and refresh your browser. 

_Questions:_
Examine the JavaScript code below your SVG. It connects two functions to mouse-events, in relation to an SVG object called
stick_figure. Add the id attribute to <svg> tag, so that it reads id="stick_figure". Try moving the mouse over your drawing. Add the properties x=0 y=0 to <svg> tag. Examine the listener keydown and the function move. Go to the browser and press the right arrow key. Check the console to see the correct key code. Do the same for the left arrow key. Replace the key codes in the move function. 
1. Move your stick figure by using the right, left arrow keys. Also, move figure up and down using respective arrow keys.
  

## Submission Instructions:
### Deadline: 29/09/20 18:00
The Submission Link is available under ASSESMENT INFORMATION/RESOURCES Section of Module Page.
### General Instruction:
Assignments must be submitted in a .zip package or alike ( .7z .bdoc .cdoc .ddoc .gtar .tgz .gz .gzip .hqx .rar .sit .tar .zip). Code submitted in other formats will not be accepted. Corrupt or otherwise unreadable files will not be accepted.

### Submission Checklist
Has your file been saved in a zip package?
Have you clicked [Submit] after uploading?
Have you checked that the file you uploaded is the correct version?
The first time you submit, you will be required to accept the Turnitin End User Licence Agreement.

After uploading, it is your responsibility to check that your file is in the correct format and that it is readable.

Late submissions will receive late penalties in line with the late penalty policy, see EECS handbook and QMUL assessment handbook.

### Specific Instructions:




## Good Luck!
