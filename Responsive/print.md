# Print

To use CSS for printing:

`media=print`

```html
		<link rel="stylesheet" type="text/css" media="screen" href="css/screen.css">
		<link rel="stylesheet" type="text/css" media="print" href="css/print.css">
```

for font-size: use **pt**. Because it's designed for printing.

set a default option for body and use `color: inherit` which means to adapt from `body`

**Example**

```css
body {
    color: black;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 12pt;
    font-weight: normal;
    margin: 0;padding:0;
}

a, a:visited{text-decoration: none;color:inherit // black }

```



## Use ::after content to set background instead of background

Normally printing in browser will initially not print the graphics (which counts as the backgrounds). However it still prints the images. In this case, we want to set the background as `an image` so the browser won't count it as a background and still prints normally. 



```css

header {
    position: relative;
}

header::after{
    content: url('../images/banner_1300_print.jpg');
    width: 19%;
}

header a.logo{display: block; width: 145px; height: 60px; position: absolute; top: 20px; left: 20px;}
header a.logo::after{content:url(../images/logo_print.svg)}
header a.logo span{
    display: none;
}

header div.hero{
    width: 75%; position: absolute; top: 110px ; left: 20px;
}
```



set header to relative and then stuff all the stuff into header using `position: absolute`

## Dealing with hyperlink

For hyperlink it's better to provide a url next to the text itself. This can be done using css `attr(name)`

**Example** :

```html
<a href="google.com">This is a link</a>
```

```css{
a::after, a:visited::after {
    content: " (" attr(href) ")";
    font-style: italic;
    word-wrap: break-word;
}
```

result:

> This is a link (*google.com*)

`attr(something)` will return a `string` as a value of that element.

**In css don't use** `+`

`word-wrap: break-word` is to make sure that if the link is too long, it will break line and go down. Not keep continuing in the same line. if we don't use word-wrap, if the link is too long it will keep continue and increase the horizontal width of the page. 



## Prevent page break inside an element

You can prevent the page break between an element when printing by:

```css
element{
    page-break-inside:avoid;
}
```

