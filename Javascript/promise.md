# Promise

Promise is use like callback, it can handle both false and complete outcome.

Next, it starts a function whenever the previous function finishes.

```javascript
let random = new Promise(function(resolve,refuse){
    let value = true;
    if(value) {
        resolve("resolve called");
        console.log(1+1);
    } else {
        refuse("refuse called");
    }
});

random.then(function(a){
    console.log(a);
}).catch(function(a){
    console.log(a);
});
```

> **result:** 
>
> 2
>
> resolve called

> Ok, if you pass something into `resolve()` or `refuse` it can be called at `a`. 

> `.then()` use when the function successfully renders. Else it's `.catch()`



**Ok let try another example**

```javascript
let first = function() {
    return new Promise(function(resolve,refuse) {
        resolve("first done ");
    });
};
let second = function(message) {
    return new Promise(function(resolve,refuse) {
        resolve(message + "second done ");
    });
};

let third = function (message) {
    return new Promise(function(resolve,refuse) {
      resolve(message + "third done");
    });
};

first().then(function(message){
    console.log("1. " + message);
    return second(message);
}).then(function(message){
    console.log("2. " + message);
    return third(message);
}).then(function(message){
    console.log("3. " + message);
    console.log(message + " finished");  
});
```

> 1. first done 
>
> 2. first done second done 
>
> 3. first done second done third done
> first done second done third done finished

so The return message in `first resolve` goes to the second. and the second goes to third.



So it wait until the first done, and then it do the second one and it do the last one.

**What if you want all of them run stimuniously together ?**

```javascript
Promise.all([first(), second(), third()]).then(function () {
    console.log("all finished");
})
```

> all finished

**What if you just want  one of them, whatever one finished.**

```javascript
Promise.race([first(), second(), third()]).then(function () {
    console.log("one of them finished");
})
```

**Another example**

```javascript
let add = function (a,b) {
    return new Promise(function (resolve,refuse){
        resolve(a+b);
    });
}

let multiply = function (a,b) {
    return new Promise(function (resolve,refuse){
        resolve(a*b);
    });
}

let divide = function (a,b) {
    return new Promise(function (resolve,refuse){
        resolve(a/b);
    });
}
var a = 3;
var b = 6;

add(a,b).then(function(result) {
    return multiply(result,5);
}).then(function(result){
    return divide(result,3);
}).then(function (result) {
    console.log(result);
});
```

> 15

