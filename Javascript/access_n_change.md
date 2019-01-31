# Access and change element

let say if we have the html

```html
<h2 class="main-title">Welcome to Moonwalk Manor</h2>
```

if you want the `innerHTML`

```javascript
document.querySelector(".main-title").innerHTML;
```

```console
"Welcome to Moonwalk Manor"
```

if you want the `outerHTML` including all of the tags:

```javascript
document.querySelector(".main-title").outerHTML;
```



## Accessing ID

if you have a html:

```html
<div id = "showcase">
    
    
</div>
```

you can easily change the `id="showcase"` to something esle:

```javascript
document.querySelector("#showcase").id = "slideshow"
```

```html
<div id = "slideshow">
    
    
</div>
```

## Accessing Class

```html
<div class="class1 class2">
    
</div>
```

For example, if you have the html above.

```javascript
document.querySelector(".class1").className
```

```console
"class1 class2"
```

`className` will return the class as a string. If you want to target each class individually, use `classList`



```javascript
document.querySelector(".class1").classList;
```

```console
["class1","class2"]
```

and then can access by:

`document.querySelector("class1").classList[0]` `document.querySelector("class1").classList[1]`

However, these two are **read-only.** 

**To change add/remove class. you need to add method**

> The two methods are `.add` and `.remove`

**Add:**

```javascript
document.querySelector(".class1").classList.add("new-class");
document.querySelector(".class1").classList;
```

```console
["class1","class2","new-class"]
```

```html
<div class="class1 class2 new-class">
    
</div>
```

**Remove**

```javascript
document.querySelector(".class1").classList.remove("class2");
document.querySelector(".class1").classList;
```

```console
["class1","new-class]
```

**Toggle**

> Turn a class on or off `.toggle("classname")`

```javascript
document.querySelector(".new-class").classList.toggle("class1");
// return false if we remove the classname.
// return true if we put the classname back.
```

**Contains**

> To check if there is a class inside an element. `.contains("classname")`

```javascript
document.querySelector(".new-class").classList.toggle("class1"); // hide class1
document.querySelector(".new-class").classList.contains("class1") // return false

document.querySelector(".new-class").classList.toggle("class1"); // put class1 back
document.querySelector(".new-class").classList.contains("class1") // return true
```

# Change attribute

`element.getAttribute("name")` returns the attribute value in `element name="value"`

`element.hasAttribute("name")` testing if the element has the attribute `name` or not

`element.setAttribute("name","value")` adding an attribute into `element`

**Example:**

```javascript
const TARGET = document.querySelector(".nav a");
if(TARGET.hasAttribute("target")) {
    console.log("The value is", TARGET.getAttribute("target"));
} else {
    TARGET.setAttribute("target","_blank");
}
```

