# variable

- start with `$`
- follow by letter or **underscore**
- can contain **letter, underscores, number or dashes**
- nospace
- case sensitive



```pph
$ITEM
$item
$myVar
$_myVar
$my-var
$__myVar
```



# Default value variable

```php
function change($color = "red") {
    echo "The color is {$color}";
}
change();
```

> The color is red

```php
change("blue");
```

> The color is blue