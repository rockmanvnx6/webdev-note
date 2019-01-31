# Callback

Callback is put a function into parameter and use that parameter as a function:

```javascript
function (a,b,callback) {
    return callback(a,b);
}
```

**Example:**

```javascript
function multiply(a,b) {
    return a*b;
}

function add(a,b) {
    return a+b;
}

function substract(a,b) {
    return a-b;
}
function calculate(a,b,callback) {
    return callback(a,b);
}

console.log(calculate(1,2,multiply));
```

