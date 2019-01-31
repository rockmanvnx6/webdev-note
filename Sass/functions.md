# functions

```scss
$colors: (
	r: red,
    b: blue
)
@function colors($name) {
    @return map-get($colors, $name);
}
```



