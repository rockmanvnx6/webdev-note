# String

**Substring**:

> Cut path of the string

`str.substring(start,end)`

```javascript
var str = "thangpham";
var cut = str.substring(0,4); // end at 4, don't count 4.
```

> than
>
> 0123

**Slice**

> This can be used for Array as well.
>
> The result is the same as **substring**

`str.slice(start,end)`

```javascript
var str = "thangpham";
var slice = str.slice(0,4);
```

> than



or when using with array

```javascript
var arr = ["this","is","me"];
var slice = arr.slice(0,3)
```

> `[‘this','is','me']`

***Slice can use with negative number, substring can't***

