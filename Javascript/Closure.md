# Closure

Closure is basically a nested function

```javascript
function doSomeMath (a,b) {
    function multiply() { // don't pass any local variables here because you want to use the global variable.
        return a * b;
    }
    return multiply;
}
```

Now, if you just type `doSomeMath();` or `doSomeMath(5,6)`

the browser will just return the `multiply` function:

```javascript
doSomeMath(6,7)
```

```console
ƒ multiply() {
        return a * b;
    }
```

if you want to get the result, you do:

```javascript
doSomeMath(6,7)();
```

now it will returns `42`

to make it easier to use, you can put it into a variable

```javascript
function doSomeMath (a,b) {
    function multiply() {
        return a * b;
    }
    return multiply;
}

var result = doSomeMath(4,5);
console.log("The result is: ",result());
```

**So what is the use of this: **

> Since you can call `variable()` to get the result. It becomes more useful to combine with multiple code.

```javascript
function doSomeMath (a,b,c) {
    function operator() {
		if(c == 1) {return a * b;}
		else if (c==0) {return a+b;}
		else {return a-b};
    }
    return operator;
}
var a = 5;
var b = 4;

var multiply = doSomeMath(a,b,1);
var add = doSomeMath(a,b,0);
var substract = doSomeMath(a,b,-1);

console.log("add: ", add());
console.log("multiply: ",multiply());
console.log("substract: ",substract());

```

```console
add:  9
multiply:  20
substract:  1
```

`typeof add` = `function`

`typeof add()` = `number`