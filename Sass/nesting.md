# nesting

```scss
body{
    background: map-get($colors, primary);
    font-family: 'Montserrat';
    margin: 0;
    #bg{
        color: map-get($colors, accent);
    }
}
```

html:

```html
<body>
    <div id="bg">
        hi
    </div>
</body>
```

