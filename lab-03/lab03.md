<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 3
</div>

### About this Lab
The purpose of this lab session is get experience working with HTML5 Canvas images and to learn transformation.

## A. Setup
1. Open [index.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-03/index.html) in browser (chrome/firefox/ie).
2. Open [index.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-03/index.html) in text editor.

## B. Draw/Position the image on the Canvas using [HTML canvas drawImage()](https://www.w3schools.com/tags/canvas_drawimage.asp) Method.

1. Download image [red_panda.jpg](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-03/red_panda.jpg).
2. Draw the image into canvas as follows; <br/>

    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var imageObj = new Image(); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; imageObj.onload=function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var destX = canvas.width / 2 - this.width / 2; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var destY = canvas.height / 2 - this.height / 2; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.drawImage(this, destX, destY); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; console.log(destX, destY); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; console.log(this.width/2, this.height/2); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }; <br/>
    
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; imageObj.src="./red_panda.jpg" <br/>

_Note the image is centered within the canvas. This is achieved by “aligning” the centres of both the canvas and the image (see variables destX and destY)._

## C. Position the image on the canvas, and specify width and height of the image using [HTML canvas drawImage()](https://www.w3schools.com/tags/canvas_drawimage.asp) Method.
1. Commnet following line. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.drawImage(this, destX, destY); <br/>
2. Add folllowing line. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ctx.drawImage(this, destX, destY, 200, 200); <br/>

## D. To do Questions
1. Crop the image in canvas using [HTML canvas drawImage()](https://www.w3schools.com/tags/canvas_drawimage.asp) Method as follows; <br/>
context.drawImage(img, sx, sy, swidth, sheight, x, y, width, height); <br/>
  * img	Specifies the image, canvas, or video element to use <br/>	 
sx	Optional. The x coordinate where to start clipping	
sy	Optional. The y coordinate where to start clipping	
swidth	Optional. The width of the clipped image	
sheight	Optional. The height of the clipped image	
x	The x coordinate where to place the image on the canvas	
y	The y coordinate where to place the image on the canvas	
width	Optional. The width of the image to use (stretch or reduce the image)	
height	Optional. The height of the image to use (stretch or reduce the image)




    



