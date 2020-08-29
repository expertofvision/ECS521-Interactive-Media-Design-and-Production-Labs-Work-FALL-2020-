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
This exercise was taken from [HTML5 Canvas Shape Events](https://konvajs.org/docs/events/Binding_Events.html).
1. Open [B.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/B.html) in browser (chrome/firefox/ie).
2. Open [B.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/B.html) in text editor.

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
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; strokeWidth: 4, <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

2. Add following events to the circle. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mouseover', function () { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseover circle'); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mouseout', function () { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseout circle'); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mousedown', function () { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mousedown circle'); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; circle.on('mouseup', function () { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; writeMessage('Mouseup circle'); <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>

3. Add the circle to the layer. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; layer.add(circle); <br/>

## E. Drag and Drop an Image
This exercise was taken from [HTML5 Canvas Drag and Drop an Image](https://konvajs.org/docs/drag_and_drop/Drag_an_Image.html).
1. Open [C.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/C.html) in browser (chrome/firefox/ie).
2. Open [C.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/C.html) in text editor.
3. Load the image as follows; <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var imageObj = new Image(); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; imageObj.onload = function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; drawImage(this); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; imageObj.src = 'cat.jpg'; <br/>
4. Add the KonvaImage in the centre of the stage and make it draggable. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var catImg = new Konva.Image({ <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; image: imageObj, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x: stage.width() / 2 - 150 / 2, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; y: stage.height() / 2 - 150 / 2, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; width: 150, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; height: 150, <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; draggable: true <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
5. Change the cursor style. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; catImg.on('mouseover', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.body.style.cursor = 'pointer'; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; catImg.on('mouseout', function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.body.style.cursor = 'default'; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); <br/>
6. Add the KonvaImage to the layer. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; layer.add(catImg); <br/>
7. Add the layer to the stage. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; stage.add(layer); <br/>

Note: the image used is [cat](https://www.flickr.com/photos/mextech/6093923823/) by [Artis Logins](https://www.flickr.com/photos/mextech/).

## F. Free Drawing
This exercise was taken from [Free Drawing Konva Demo](https://konvajs.org/docs/sandbox/Free_Drawing.html).
1. Open [D.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/D.html) in browser (chrome/firefix/ie).
2. Open [D.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-05/D.html) in text editor.
3. Read the code and understand it.
4. Add options to change and use at leaset 3 different brush colour.
5. Add an option to clear the whole canvas at once.

**Submission Instructions:** To be added......................


## Good Luck!














