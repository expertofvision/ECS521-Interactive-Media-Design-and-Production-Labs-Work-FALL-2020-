<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 3
</div>

### About this Lab
This lab focuses on adding interactive animation to HTML5 canvas using [Konva.js](https://konvajs.org/), a HTML5 2d canvas library.

## A. How does it works?
1. Every thing starts from Konva.Stage that contains several user’s layers (Konva.Layer) [1](https://konvajs.org/docs/overview.html). 
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



