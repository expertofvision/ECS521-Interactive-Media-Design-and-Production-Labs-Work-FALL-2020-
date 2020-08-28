<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 5
</div>

### About this Lab
This lab focuses on adding interactive animation to HTML5 canvas using [Konva.js](https://konvajs.org/), a HTML5 2d canvas library.

## A. How does it works?
1. Every thing starts from Konva.Stage that contains several user’s layers (Konva.Layer) [[1]](https://konvajs.org/docs/overview.html). 
2. Each layer can contain shapes, groups of shapes, or groups of other groups.

## B. Setup
1. Open [A.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/A.html) in browser (chrome/firefox/ie).
2. Open [A.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/A.html) in text editor.
3. Read and understand how a stage and a layer are created.

## C. Adding Mouse event to the whole stage
1. Add a mouseout event to the stage. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stage.on('mouseout', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseout canvas'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; });

2. Add a mousemove event to the stage and display the mouse position. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stage.on('mousemove', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var mousePos = stage.getPointerPosition(); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var x = mousePos.x - 190; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var y = mousePos.y - 40; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('x: ' + x + ', y: ' + y); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
    
## D. Associate events with different shapes on a canvas 
This exercise was taken from HTML5 Canvas Shape Events.
1. Open B.html in browser (chrome/firefox/ie).
2. Open B.html in text editor.

### Draw a triangle as follows; <br/>
1. Add following triangle drawing function. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var triangle = new Konva.RegularPolygon({ <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x: 80, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; y: 120, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sides: 3, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; radius: 80, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fill: '#00D2FF', <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stroke: 'black', <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; strokeWidth: 4 <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

2. Add a mouseout event to the triangle. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; triangle.on('mouseout', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseout triangle'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

3. Add a mousemove event to the triangle and display the mouse position. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; triangle.on('mousemove', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var mousePos = stage.getPointerPosition(); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var x = mousePos.x - 190; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var y = mousePos.y - 40; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('x: ' + x + ', y: ' + y); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

4. Add the triangle to the layer. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; layer.add(triangle); <br/>

### Draw circle as follows; <br/>
1. Add following circle drawing function. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var circle = new Konva.Circle({ <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x: 230, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; y: 100, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; radius: 60, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fill: 'red', <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stroke: 'black', <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; strokeWidth: 4 <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

2. Add following events to the circle. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mouseover', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseover circle'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mouseout', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseout circle'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mousedown', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mousedown circle'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mouseup', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseup circle'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

3. Add the circle to the layer. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; layer.add(circle); <br/>













