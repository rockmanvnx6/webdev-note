# Condition in if else statement.

Ok so, if else in javascript is the same in C

```javascript
if (your mom is gay) {
    your dad is trans;
} else {
    its ok;
}
```

However let say:

```javascript
var a = 5;
var b = '5';

if(a==b) {
    document.body.innerHTML = "EAT DOGS";
} else {
    document.body.innerHTML = "don't eat dogs";
}
```

`EAT DOGS`

**Why ?** 

> because when you pass in a==b. Javascript will think **oh, you mean comparing number to number, lemme convert that `b` into a number for you, boss.**

However, sometime you don't want to do that, you want the *Exact comparison*.

```javascript
var a = 5;
var b = '5';

if(a===b) {
    document.body.innerHTML = "EAT DOGS";
} else {
    document.body.innerHTML = "don't eat dogs";
}
```

`don't eat dogs`

likewise, we have *strict inequality*:

`!==`

```javascript
if (a !== b) {
    document.body.innerHTML = "concho";
} else {
    document.body.innerHTML = "deptrai";
}
```

`deptrai`



# Ternary Operator

```javascript
condition ? true : false
// example:
a == b ? document.body.innerHTML = 'eat shit' : document.body.innerHTML = 'eat ass'
```



*the rest is like c*