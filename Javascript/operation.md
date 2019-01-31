# Operation

Javascript is somewhat like python. when you use:

```javascript
var a = 5;
var b = '4';
var sum = a+b
```

`sum = '54'`

now sum is defined as string.



However, if you try:

```javascript
sum = a*b
//or
sum = a-b
//or
sum = a/b
```

Javascript will automatically assume that you want to use `b` as `number` and then it automatically `convert b into number` and perform the operation.

`sum = 20`

`sum =  -1`

`sum = 1.25`



However if you say

```javascript
var a = 1;
var b = "hello";
var sum = a-b
```

it will return `sum = NaN` - `not a number`

