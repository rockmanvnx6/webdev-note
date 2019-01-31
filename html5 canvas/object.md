# Objects

assume you already have:

```javascript
let canvas = document.querySelector("canvas");
```



To create a new object: 

```javascript
var object = canvas.getContext('2d');
```



Now you can make it to be a rectangle, circle, etc.



## fillRect();

`fillRect` will transform the object into a rectangle.

```javascript
object.fillrect(x,y,width,height)
```

example:

```javascript
object.fillrect(50,50,100,100)
```

> left: 50px;
>
> top: 50px;
>
> width: 100px;
>
> height: 100px;

To change color: **add before fillrect**

```javascript
object.fillStyle = "blue/red/rgba()/#.."
```



## Stroke

To draw a line, stroke.

Initial - start drawing. **If there is any connector from the previous path, this might be the case. Put it again to start a new shape.**

```javascript
object.beginPath();
```

Start point:

```javascript
object.moveTo(x,y)
```

End point:

```javascript
object.lineTo(x,y)
```

Draw:

```javascript
object.stroke()
```

To change color: **Add before Draw**

```javascript
object.strokeStyle="blue/red/rgba()/#.."
```

## Circle

```javascript
object.arc(x,y,radius,start_radian,end_radian, clockwise-boolean)
```

examble:

```javascript
object.arc(300,300,30,0,Math.PI*2,false);
```

and then to draw, use either **stroke or fill**

```javascript
object.stroke();
```

to fill:

```javascript
object.fillstyle="color";
object.fill();
```



**Full example:**

```javascript
object.beginPath() // seperate from previous shape
object.arc(300,300,30,0,Math.PI*2,false);
object.stroke();
object.fillstyle="red";
object.fill();
```



**Intergrate with for loop**

```javascript
let fullwidth = window.innerWidth;
let fullheigh = window.innerHeight;
for(var i = 0; i < 30; i++){
    object.beginPath();
    object.arc(Math.random()*fullwidth,Math.random()*fullheigh,Math.random()*30+1,0,Math.PI*2,false);
    object.strokeStyle="black";
    object.stroke();
    object.fillStyle="red";
    object.fill();
}
```

## LineWidth

To set the linewidth of a shape

`object.lineWidth=10`

then **stroke**.