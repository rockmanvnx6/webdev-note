# Array

Basically it's like python.

```javascript
var pens = ["red", "blue", "green", "orange"];
var pen1 = new Array("red","blue","green");
console.log(pen1);
console.log(pens);
```

```console
["red", "blue", "green"]
["red", "blue", "green", "orange"]
```



in here you can see there is a long way:

`var pen1 = new Array()` 

this is to create a new Array type object and assign it to `pen1`.

#### Mixed array:

In Javascript, you can mix any type into your array:

```javascript
var c = ["string",19,true,"another string shit"];
```



`typeof array == object `



Access to array element like python and c.



```javascript
for (i = 0; i < c.length; i++) {
    console.log(c[i]);
}
```

```console
string
19
true
another string shit
```



## Array properties:

If you create an array and use console.log to see. You will see things like this:

```console
0: "string
1: 19
2: true
3: "another string shit"
length: 4;
```

This is the array properties. we can get the object by:

`array.properties`

in example:

`c.length`, `c[0]`, `c[1]`,`c[2]`,`c[3]`. 



## ARRAY METHOD

Not like C, javascript is much easier.

### Reverse

`array.reverse()`

```javascript
var c = [1,2,3,4,5];
c.reverse;
console.log(c);
```

`[5,4,3,2,1]`

```javascript
var c = [1,3,4,2,5];
c.reverse;
console.log(c);
```

`[5,2,4,3,1]`

```javascript
var c = ['a','b','c','d','e'];
c.reverse();
console.log(c);
```

`[‘e','d','c','b','a']`

### Adding / Removing

#### From head:

**Remove:**

`array.shift()`

> this will return the object that has been ‘shifted' and modify the original array.

```javascript
var arr = ["a","b","c","d"];
arr.shift(); //return "a"
console.log(arr);
```

`["b","c","d"]`

**Add:**

`array.unshift()`

> This will return the **length** of the array after execution.

```javascript
var arr = ["a","b","c","d"];
arr.unshift("e"); //return 5
console.log(arr);
```

`["e","a","b","c","d"]`

or can even do 

```javascript
var arr = ["this","is"];
arr.unshift("item1","item2","item3",..);
```

`["item1","item2","item3","this","is"]`



#### From tail

**Remove:**

`array.pop()`

```javascript
var c = [1,2,3,4,5]
c.pop() // return 5
console.log(c);
```

`[1,2,3,4]`

**Add:**

`array.push()`

```javascript
var c = [1,2,3,4,5]
c.push(6); // return 6 - the number of element
console.log(c);
```

`[1,2,3,4,5,6]`

```javascript
var c = ['a','b','c'];
c.push('d'); // return 4
console.log(c);
```

`[‘a','b','c','d']`

or can push multiple item:

```javascript
var c = [1,2,3];
c.push(5,3,2,1,4,56,99);
console.log(c);
```

`[1, 2, 3, 5, 3, 2, 1, 4, 56, 99]`

### Remove a specific item

What if you want to specifically remove 1 item from an array? 

```javascript
var arr = ["orange", "apple", "watermelon", "nigga"]
```

now what if i want to remove `watermelon` ?

Use : `array.splice(start,number_of_item_you_want_to_remove_count_it_self)`

```javascript
// start at index 2, remove 1 item at index 2
arr.splice(2,1); // return ["watermelon"]
console.log(arr);

```

`["orange", "apple", "nigga"]`



### Copy

`var new_arr = arr.slice()`

```javascript
var arr = ['a','b','c','d','e'];
var new_arr = arr.slice()
console.log(new_arr)
```

`[‘a','b','c','d','e']`



### Search

To search for a specific item in an array and return `index` if found, `-1` if can't find:

`array.indexOf(item,search_from_index)`

```javascript
var arr = ['a','b','c','d','e','f']
var search = arr.indexOf('d',0); // search from the beginning
console.log(search);
```

`3`

```javascript
var arr = ['a','b','c','d','e','f']
var search = arr.indexOf('d',2); // search from index 2
console.log(search);
```

`3`

```javascript
var arr = ['a','b','c','d','e','f']
var search = arr.indexOf('d',5); // search from index 5
console.log(search);
```

`-1` - can't find.



### Join

Join an array into a string:

`array.join(seperator)`

```javascript
var arr = ["thang","kieu","nip","trinh","tam"];
var shit = arr.join();
console.log(shit);
console.log(typeof shit);
```

`thang,kieu,nip,trinh,tam`

`string`

```javascript
var arr = ["thang","kieu","nip","trinh","tam"];
var shit = arr.join(', ');
console.log(shit);
console.log(typeof shit);
```

`thang, kieu, nip, trinh, tam`

`string`

```javascript
var arr = ["thang","kieu","nip","trinh","tam"];
var shit = arr.join('=*|*=');
console.log(shit);
console.log(typeof shit);
```

`thang=*|*=kieu=*|*=nip=*|*=trinh=*|*=tam`

`string`

```javascript
var arr = [1,2,3,4,4];
var shit = arr.join();
console.log(shit);
console.log(typeof shit);
```

`1,2,3,4,4`

`string`

