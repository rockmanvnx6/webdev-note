# Math random

to get negative:

```javascript
Math.random() - 0.5;
```

>  Max: 0.5. Low: -0.5





```javascript
function randomIntFromRange(min,max) {
  return Math.floor(Math.random()*(max-min+1) + min);
}
```

