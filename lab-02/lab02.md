<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 2
</div>

### About this Lab
This lab is about styling a canvas and simulating depth.

## A. Setup
1. Open [index.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-02/index.html) file in browser (chrome/firefox/ie).
2. Open [index.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-02/index.html) and [sky.js](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-02/sky.js) files in a text editor.
3. Create a new file layout.css using text editor.

### Adapt canvas to windows size 
1. Notice there is a space between the beginning of the web page and where the canvas is displayed.
2. Eliminate this space by adding the following rule to layout.css file; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; html, body { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; width: 100%; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; height: 100%; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; margin: 0; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; border: 0; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; overflow: hidden; /* Disable scrollbars */ <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; display: block; /* No floating content on sides */ <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>

3. Make the canvas fit 100% of the page by adding the following rule to layout.css file.

    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; canvas { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; width: 100%; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; height: 100%; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; position: absolute; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>

## B. Scale canvas when window is resized
Here we will use the window property devicePixelRatio that “returns the ratio of the resolution in physical pixels to the
resolution in CSS pixels for the current display device. This value could also be interpreted as the ratio of pixel sizes: the size of one
CSS pixel to the size of one physical pixel. In simpler terms, this tells the browser how many of the screen’s actual pixels should be
used to draw a single CSS pixel.” [[1]](https://developer.mozilla.org/en-US/docs/Web/API/Window/devicePixelRatio). 

1. Add the following line at beginning sky.js; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var scale = window.devicePixelRatio; <br/>

2. Go to the definition of redraw function. Add the following lines to get the CSS width and height of the canvas and scale it using the variable defined in the previous step [[2]](https://medium.com/wdstack/fixing-html5-2d-canvas-blur-8ebe27db07da). <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let style_width = +getComputedStyle(bg_canvas).getPropertyValue("width").slice(0, -2) * scale; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let style_height = +getComputedStyle(bg_canvas).getPropertyValue("height").slice(0, -2) * scale; <br/>

3. Change the calls to drawBackground and drawForeground so they read; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; drawBackground(style_width, style_height); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; drawForeground(style_width, style_height); <br/>

4. Go to the definition of drawBackground function and set the size of the canvas at the beginning; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; bg_canvas.setAttribute('width', width); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; bg_canvas.setAttribute('height', height); <br/>

5. Go to the definition of drawForeground function and set the size of the canvas at the beginning; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fg_canvas.setAttribute('width', width); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fg_canvas.setAttribute('height', height); <br/>

## C. Add more Objects
1. Go to the definition of drawForeground function.
2. Add an [albatross image](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-02/37586.png) as follows; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; albatross_img = new Image(); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; albatross_img.src = '37586.png'; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; albatross_img.onload = function(){ <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fg_ctx.drawImage(albatross_img, 200, 200); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>

3. Draw a couple of clouds by invoking the function drawCloud(startX, startY, alpha) as follows; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let numClouds = 10; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; for (let i = 1; i < numClouds; i++) <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; drawCloud(100 * i , 50 * i + 120 , i / numClouds); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>

## D. To do Questions

1. Notice the alpha argument sets the transparency of the cloud. Modify function drawCloud(); [Help](https://www.w3schools.com/tags/ref_canvas.asp) <br/>
    a) Tune this function for transparency. <br/>
    b) Change starting point of clouds. <br/>
    c) Change colour of clouds. <br/>
2. Creat your own different shape cloud. <br/>
    a) using [HTML canvas bezierCurveTo()](https://www.w3schools.com/tags/canvas_beziercurveto.asp) Method. <br/>
    b) using [HTML canvas quadraticCurveTo()](https://www.w3schools.com/tags/canvas_quadraticcurveto.asp) Method. <br/>

#### Help: You can also use [bezierCurveTo command generator](http://www.victoriakirst.com/beziertool/), if you are more familiar with JavaScript and Canvas.

## Submission Instructions:
### Deadline: 06/10/20 18:00
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
1. To get half of the marks, your code should be fully functional with atleast Question No. 1 solved completely.

## Good Luck!














