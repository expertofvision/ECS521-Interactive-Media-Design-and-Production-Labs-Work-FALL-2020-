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

## Draw image in Canvas

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

