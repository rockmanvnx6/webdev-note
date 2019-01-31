# General Rule

if you want the script to run before the content of the web:

`add it to head`

if you want the script to run after the content of the web:

`add it to the body`



**Example:**

```html
<!DOCTYPE html>
<html lang="en-US">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>An empty page</title>
    <script>
            var date = new Date();
            document.body.innerHTML = "<h1> Today is: " + date + "</h1>";
    </script>
</head>

<body>
 
</body>

</html>
```

`return ERROR`

###### Why ?

> because it runs from the head to the bottom. it hasn't render the body yet and the script is running already.

When we use script link:

>The website will download the script first and load the script content then load the html content. Pause the body first to load the script.
>This is called render blocking
>It's a good practice to put javascript at the **bottom of the page.**



=> put `<script src="script.js"></script>` at the bottom of the page.

or we can use **Asynchronous**

# Asynchronous

Make the javascript download the same time it is reading html parsing.

```html
<script src="script.js" async></script>
```

adding the tag `async` tells it to do that. So we don't have to wait till it load the whole javascript.

and the script only **happens where it's called.**



# Deferred

Run javascript **after everthing else is loaded**

It also download javascript the same time it is reading html.

```html
<script src="script.js" defer></script>
```



back in the example above, we can state:

```html
<!DOCTYPE html>
<html lang="en-US">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>An empty page</title>
    <script src="script.js" defer></script>

</head>

<body>

</body>
</html>

```

# Syntax Rule

```javascript
// Variables start with lower case letter:
var greenDuck;

// Objects and classes start with uppercase letter:
var date = Date();

// Constants are all-caps:
const = CONSTANTLYUPPERCASE
```



