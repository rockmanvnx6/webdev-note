## String concatenate - see basic function



# strtolower(`string`)

> Lower case the string

```php
<?php
    $string = "this is how you do it.";
    echo strtolower($string);
?>
```

> this is how you do it.

## strtoupper(`string`)

> Uppercase the whole string

```php
<?php
    $string = "this is how you do it.";
    echo strtoupper($string);
?>
```

> THIS IS HOW YOU DO IT.

## ucfirst(`String`)

> Upper case first character

```php
<?php
    $string = "this is how you do it.";
    echo ucfirst($string);
?>
```

> This is how you do it.



## ucwords(`string`)

> Upper case words

```php
<?php
    $string = "this is how you do it.";
    echo ucwords($string);
?>
```

> This Is How You Do It.





## strlen(`string`)

> return string length



## trim(`string`)

```php
echo "A". trim(" B C D ") . "E";
```

```php
AB C DE
```



## strstr(`string`,`word`)

> Substring from `string`

```php
<?php
    $string = "this is how you do it.";
    echo strstr($string,"is");
?>
```

```php
is is how you do it.
```



## strchr (`string`,`char`)

> Substring from `string`

```php
<?php
    $string = "this is how you do it.";
    echo strchr($string,"i");
?>
```

```php
is is how you do it.
```



## str_replace(`original word`,`substitutional word`,`string`)

> replace `original word` to `substitutional word` in `string`

```php
<?php
    $string = "this is how you do it.";
    echo str_replace("is","are",$string)
?>
```

```php
thare are how you do it.
```



## str_repeat(`string`,`number of repetition`)

```php
<?php
    $string = "this is how you do it.";
    echo str_repeat($string,2)
?>
```

```php
this is how you do it. this is how you do it.
```



## substr(`string`,`from index`, `to index`)

```php
<?php
    $string = "this is how you do it.";
    echo substr($string,2,3)
?>
```

```php
is
```





## strpos(`string`,`word`)

> return the first index that contains `word`

```php
<?php
    $string = "this is how you do it.";
    echo strpos($string,"how");
?>
```

> 8