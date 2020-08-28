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
var triangle = new Konva.RegularPolygon({ <br/>
x: 80, <br/>
y: 120, <br/>
sides: 3, <br/>
radius: 80, <br/>
fill: '#00D2FF', <br/>
stroke: 'black', <br/>
strokeWidth: 4 <br/>
}); <br/>

2. Add a mouseout event to the triangle. <br/>
triangle.on('mouseout', function() { <br/>
writeMessage('Mouseout triangle'); <br/>
}); <br/>

3. Add a mousemove event to the triangle and display the mouse position. <br/>
triangle.on('mousemove', function() { <br/>
var mousePos = stage.getPointerPosition(); <br/>
var x = mousePos.x - 190; <br/>
var y = mousePos.y - 40; <br/>
writeMessage('x: ' + x + ', y: ' + y); <br/>
}); <br/>

4. Add the triangle to the layer. <br/>
layer.add(triangle); <br/>

### Draw circle as follows; <br/>
1. Add following circle drawing function. <br/>
var circle = new Konva.Circle({ <br/>
x: 230, <br/>
y: 100, <br/>
radius: 60, <br/>
fill: 'red', <br/>
stroke: 'black', <br/>
strokeWidth: 4 <br/>
}); <br/>

2. Add following events to the circle. <br/>
circle.on('mouseover', function() { <br/>
writeMessage('Mouseover circle'); <br/>
}); <br/>
circle.on('mouseout', function() { <br/>
writeMessage('Mouseout circle'); <br/>
}); <br/>
circle.on('mousedown', function() { <br/>
writeMessage('Mousedown circle'); <br/>
}); <br/>
circle.on('mouseup', function() { <br/>
writeMessage('Mouseup circle'); <br/>
}); <br/>

3. Add the circle to the layer. <br/>
layer.add(circle); <br/>













