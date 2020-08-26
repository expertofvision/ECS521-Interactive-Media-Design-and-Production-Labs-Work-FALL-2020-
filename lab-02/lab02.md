<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 2
</div>

### About this Lab
This lab is about styling a canvas and simulating depth.

### A. Setup
1. Open index.html file in browser (Chrome/Firefox/IE).
2. Open index.html, layout.css and sky.js files in a text editor.

## Adapt canvas to windows size 
1. Notice there is a space between the beginning of the web page and where the canvas is displayed.
2. Eliminate this space by adding the following rule to layout.css file;

html, body { <br/>
width: 100%; <br/>
height: 100%; <br/>
margin: 0; <br/>
border: 0; <br/>
overflow: hidden; /* Disable scrollbars */ <br/>
display: block; /* No floating content on sides */ <br/>
} <br/>

## 3. Make the canvas fit 100% of the page by adding the following rule to layout.css file.

canvas { <br/>
width: 100%; <br/>
height: 100%; <br/>
position: absolute; <br/>
} <br/>








