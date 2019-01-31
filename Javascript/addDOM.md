# Add DOM element

What if you want to add an html element inside an html element ?

let say:

```html
<figure class="featured-image">
    <img src="images/testimonials/bluepebble.jpg" alt="Earthrise: A photograph of the Earth and parts of the Moon's surface taken by astronaut William Anders in 1968, during the Apollo 8 mission.">
</figure>
```

Now you want to make something like this:

```html
<figure class="featured-image">
    <img src="images/testimonials/bluepebble.jpg" alt="">
    <figcaption>Earthrise: A photograph of the Earth and parts of the Moon's surface taken by astronaut William Anders in 1968, during the Apollo 8 mission.</figcaption>
</figure>
```



**In this lesson we will use 3 methods:**

`document.createElement("element")` create a new `<element></element>`

`document.createTextNode("text")` create a html node to add into `element`

so in general it will be `<element> TextNode </element>`

`element.appendChild();` append a `childnode` into an `element`

```javascript
// first, let declare a constant so code don't get duplicated
const FEATURED = document.querySelector(".featured-image");
const IMG = FEATURED.querySelector("img"); // so don't have to traverse from head.
var altVar = IMG.getAttribute("alt"); // value of the alt attribute;
var element = document.createElement("figcaption"); // <figcaption></figcaption>
var textNode = document.createTextNode(altVar); // 
element.appendChild(textNode); // <figcaption> textNode </figcaption>
FEATURED.appendChild(element); 
// <figure class="featured....<figcaption>..</figcaption></figure>
IMG.setAttribute("alt","") // empty.
```

***HTML contains a element node and a text node***

##### Another method:

> This method is not supported by old browsers.

`append()`- append anystring into a node. So you don't have to create a `textnode` anymore.

```javascript
const FEATURED = document.querySelector(".featured-image");
const IMG = FEATURED.querySelector("img"); 
var altVar = IMG.getAttribute("alt");
var element = document.createElement("figcaption");
// var textNode = document.createTextNode(altVar); 
element.append(altVar);
FEATURED.append(element);
IMG.setAttribute("alt","") // empty.
```

