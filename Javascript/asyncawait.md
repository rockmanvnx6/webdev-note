# Async - Await

When a function is called an `async function` , it **allows other function** to run through it **without waiting for it to return ** although being called first.

*Example:*

```javascript
asyncCall();
normalCall(); // still execute even asyncCall hasn't finished.
```

## Await and Promise

Await is only available in *Async function*

> Await is a way to **trigger** a **Promise** function
>
> The Promise function will promise to return the value.
>
> While waiting the promise function to return the value, async function will make sure that other functions will run smoothly without waiting.
>
> **await** will make sure that when promise is done, it continues the next block of the code.

*Example*

```javascript
async function asyncCall() {
    console.log("called async call");
    var result = await anotherFunction();
    console.log(result)
}

function anotherFunction () {
    return new Promise((resolve) => {
        resolve(1+1)
    })
}
```

inside the `Promise()` is a `resolve`. The value that the promise function return has to be wrapped by `resolve`

Say If you leave async function on hang and call another function

```js
function resolveAfter2seconds() {
	return new Promise(item => {
		setTimeout(() => {
			item(1+1)
		},2000)
	});
}

async function asyncCall() {
	console.log("calling");
	var result = await resolveAfter2seconds();
	console.log(result);
	console.log("something else")
}

function normalFunction() {
	console.log("called normal function")
}

asyncCall()
normalFunction()

```

> calling
> called normal function
> 2
> something else

## Using await to call parallel

To call parallel, you might not want to assign it to a `var` and later console.log the var like the example above. This will postpone the code block and only executes when the previous await is finish.

```js
var continue1 = () => { 
    return new Promise(resolve => {
        setTimeout(() => {
            resolve (10);
            console.log("continue1 is called");
        },500)
        
    })
}


var continue2 = () => {
    return new Promise(resolve => {
        resolve(20);
        console.log("continue2 is called");
    })
}


var main = async () => {
    let value1 = continue1();
    let value2 = continue2();

    console.log(await value1);
    console.log(await value2)
}

main();
```

in here, each `value` stores a `Promise` and `await` is then moved to `console.log` to make sure that both functions `continue` are running asynchronously.

> continue2 is called
> continue1 is called
> 10
> 20

However, if changing main to 

```js
var main = async () => {
    let value1 = await continue1();
    let value2 = await continue2();

    console.log(value1);
    console.log(value2)
}
```

the values are:

> continue1 is called
> continue2 is called
> 10
> 20

## Using Promise.all()

a better way to call it concurrently is to use `Promise.all()` instead of `await`

Changing `main()` from:

```js
var main = async () => {
    let value1 = continue1();
    let value2 = continue2();

    console.log(await value1);
    console.log(await value2)
}
```

to

```js
var main = async () => {
    Promise.all([continue1(), continue2()]).then(message => {
        console.log(message)
    })
}
```

will give the exact same result.

> continue2 is called
> continue1 is called
> [ 10, 20 ]

In which all `resolve` now are stored in `message`, which is an array.

## Parallel with Promise.then()

Notice that both `continue` functions are returning a promise.

Thus we can use `.then()`

changing main to:

```js
var main = async () => {
    continue1().then(message => console.log(message));
    continue2().then(message => console.log(message));
}
```

Result:

> continue2 is called
> 20
> continue1 is called
> 10

`message` is now act as `resolve`