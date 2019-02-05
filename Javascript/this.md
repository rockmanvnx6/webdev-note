# `This` keyword

By default, if `console.log(this)` in browser. It's `window` object.

In terminal - when using `node` it's `undefined`

## In object

When `this` in object, it refers to the object itself

```js
var myObj = {
    value: 10,
    someFunction: function() {
        console.log(this);
    }
}
```

> Return myObj

## As a constructor

```js
function myObj(firstName, lastName) {
    this.firstName = firstName;
}

var object = new myObj("thang","pham");
object.firstName // thang
```

## In Immediately Invoked Function expression

```js
(function () {
    console.log(this)
})();
```

In IIFE, it always be the `window` for browser and `global settings` for node.

## In EventListener

In Event listener, `this` refers to the item that being clicked on.

```js
document.getElementById("submit").addEventListener("click", function fireEvent() {
    console.log(this)
}, false);
```

this will refer to the DOM that being clicked on.

On the other hand, we can also do like this:

```js
document.getElementById("submit").addEventListener("click", fireEvent, false);
function fireEvent() {
    console.log(this)
}
```

or this also works:

```js
document.getElementById("submit").addEventListener("click", function() {
    console.log(this)
}, false);
```

However arrow function will refer `this` to `window`

```js
document.getElementById("submit").addEventListener("click", () => {
    console.log(this)
}, false);
```

## Arrow function

In arrow function `this` is set to the global object `window`