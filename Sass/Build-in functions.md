# Built-in function

## Map-get

```scss
$color: (
	primary: #213020,
    accent: #210222
);

body{
    color: map-get($color,primary);
}
```

## Lighten: // in CSS

> Lighten a color

```scss
body{
    color: lighten(#005DFF, 40%);
}
```



## Darken: // in css

> Darken a color
```scss
body{
    color: darken(#005DFF, 40%);
}
```
## Max: // in css

> Finding the minimum value allowed for a property