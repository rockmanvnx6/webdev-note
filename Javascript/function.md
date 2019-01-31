# Function

In javascript you don't have to declare function type

```javascript
function multiply(a,b) { 
	var result = a*b;
    console.log(result);
    retrun result;
}

var multiplied = multiply(3,4);
```

3 types of functions:

**Regular function**

```javascript
function multiply() {
    var result = 3 * 4;
    console.log("3 multiplied by 4 is ", result);
}
multiply();
```

`3 multiplied by 4 is  12`

**Anonymous function**

> Function within a variable. Invoked (called) by calling the variable as a function

```javascript
var callme = function () {
    var result = 4+1;
    console.log(result)
}
callme();
```

`5`

**Immediately Invoked Function Expression**

> Run as soon as the browser finds it.

```javascript
(function () {
  var result = 2+2;
  console.log(result);
}());
```

`4`





###### Example:

```javascript
function findBiggestFraction(a,b) {
    var result;
    a>b ? result = ['firstFraction',a] : result = ['secondFraction',b];
    console.log(result);
    return result;
}

var firstFraction = 3/4;
var secondFraction = 5/7;

var result = findBiggestFraction(firstFraction,secondFraction);
console.log("The larger element is: " + result[0] + ". Which has the value of: " 
+ result[1]);
```

`The larger element is: firstFraction. Which has the value of: 0.75`



## Study case:

```javascript
var a = 3;
var b = 6;

var theBiggest = function (a,b) {
    var result;
    a > b ? result = a : result = b;
    return result;
}
console.log("The biggest is: ", theBiggest(a,b));
```

`The biggest is:  6`



Notice that when you want the variable in the function, you have to call `theBiggest()`

Is there anyway you can call it without the `()` and make it like an actual variable?



Yes, use *immediately invoked function*

```javascript
var a = 3;
var b = 6;
var result = (function (a,b){
    var result1;
    a > b ? result1 = a : result1 = b;
    return result1;
}(a,b));

console.log(result);
```

`6`

