# DOM

`window` is an object

inside window we have `document`

can target by `window.document`

However `document` itself is also an object

## Document

```javascript
document.body; //body element
document.title; // title of the web
document.URL; // URL of the web

document.getElementsById("someID") // get by ID
document.getElementsByClassName("Classname") // get class .abcde
document.getElementsByTagName("html tag")// b, a,..
```

```javascript
/* First element matching specified selector(s) */
document.querySelector(".main-nav a"); // css selector
/* All element matching specified selector(s) */
document.querySelectorAll(".post-content a"); // css selector
```

**Example**:

```javascript
document.querySelectorAll(".social-nav a[href*='linkedin.com']")
```

```console
NodeList [a.icon-linkedin]0: a.icon-linkedinaccessKey: ""assignedSlot: nullattributeStyleMap: StylePropertyMap {size: 1}attributes: NamedNodeMap {0: class, 1: href, 2: style, class: class, href: href, style: style, length: 3}autocapitalize: ""baseURI: ...
```

```javascript
document.querySelectorAll(".menu li a, .social-nav li a");
/* gives information from both */
```

