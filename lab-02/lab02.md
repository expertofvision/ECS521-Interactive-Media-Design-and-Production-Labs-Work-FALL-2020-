<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 2
</div>

### About this Lab
This lab is about styling a canvas and simulating depth.

## A. Setup
1. Open index.html file in browser (Chrome/Firefox/IE).
2. Open index.html, layout.css and sky.js files in a text editor.

### Adapt canvas to windows size 
1. Notice there is a space between the beginning of the web page and where the canvas is displayed.
2. Eliminate this space by adding the following rule to layout.css file;

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; html, body { <br/>
width: 100%; <br/>
height: 100%; <br/>
margin: 0; <br/>
border: 0; <br/>
overflow: hidden; /* Disable scrollbars */ <br/>
display: block; /* No floating content on sides */ <br/>
} <br/>

3. Make the canvas fit 100% of the page by adding the following rule to layout.css file.

canvas { <br/>
width: 100%; <br/>
height: 100%; <br/>
position: absolute; <br/>
} <br/>

## B. Scale canvas when window is resized
Here we will use the window property devicePixelRatio that “returns the ratio of the resolution in physical pixels to the
resolution in CSS pixels for the current display device. This value could also be interpreted as the ratio of pixel sizes: the size of one
CSS pixel to the size of one physical pixel. In simpler terms, this tells the browser how many of the screen’s actual pixels should be
used to draw a single CSS pixel.” [1] 

1. Add the following line at beginning sky.js;
var scale = window.devicePixelRatio; <br/>

2. Go to the definition of redraw function. Add the following lines to get the CSS width and height of the canvas and scale it using the variable defined in the previous step [2].
let style_width = +getComputedStyle(bg_canvas).getPropertyValue("width").slice(0, -2) * scale; <br/>
let style_height = +getComputedStyle(bg_canvas).getPropertyValue("height").slice(0, -2) * scale; <br/>

3. Change the calls to drawBackground and drawForeground so they read;
drawBackground(style_width, style_height); <br/>
drawForeground(style_width, style_height); <br/>

4. Go to the definition of drawBackground function and set the size of the canvas at the beginning;
bg_canvas.setAttribute('width', width); <br/>
bg_canvas.setAttribute('height', height); <br/>

5. Go to the definition of drawForeground function and set the size of the canvas at the beginning;
fg_canvas.setAttribute('width', width); <br/>
fg_canvas.setAttribute('height', height); <br/>

## C. Add more Objects
1. Go to the definition of drawForeground function.
2. Add an albatross image as follows;

albatross_img = new Image(); <br/>
albatross_img.src = '37586.png'; <br/>
albatross_img.onload = function(){ <br/>
fg_ctx.drawImage(albatross_img, 200, 200); <br/>
} <br/>

3. Draw a couple of clouds by invoking the function drawCloud(startX, startY, alpha) as follows;

let numClouds = 10; <br/>
for (let i = 1; i < numClouds; i++) <br/>
{ <br/>
drawCloud(100 * i , 50 * i + 120 , i / numClouds); <br/>
} <br/>

## D. To do Questions

1. Notice the alpha argument sets the transparency of the cloud. Tune it to make bird more visible.
2. Creat your own cloud using HTML canvas bezierCurveTo() and HTML canvas quadraticCurveTo() Methods. Note: The bird should be more visible.

#### Help: You can also use bezierCurveTo command generator, if you are more familiar with JavaScript and Canvas.














