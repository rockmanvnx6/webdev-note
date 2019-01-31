# Animation

To make something animate:

```javascript
function animate() {
    requestAnimationFrame(animate);
    /* what to animate */
}
```

Basically this will create a loop continuously call animate().

example:

```javascript
var x =0;
function animate() {
    requestAnimationFrame(animate);
    object.clearRect(0,0,innerWidth,innerHeight); //blank rect to clear;
    object.fillRect(x+=1,0,120,120);
}
animate();
```

