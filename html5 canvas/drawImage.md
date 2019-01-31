# DrawImage

```javascript
var canvas = document.querySelector("canvas");
var c = canvas.getContext("2d");

var img = new Image();
img.src = "../src/link_to_img.jpg";

c.drawImage(img,Source_x,Source_y,Source_width,Source_height,X,Y,Width,Height)
```

> **Source_x, Source_y:** In the original image, where to cut.
>
> **Source_width, Source_height:** In the original image, **how big is the clip**
>
> **X, Y:** Where in the canvas (the big one) you want the image to be put.
>
> **Width, Height**: How are the width and height is the clipping image **according to the canvas.**

