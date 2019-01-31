# Variable

```scss
$mycolor: #341def;

body{
    background: $mycolor
}
```



## Multiple colors sass map



```scss
$colors: (
    primary: #005DFF,
    accent: #FFF6BB
);

body{
    background: map-get($colors, primary);
}
```

