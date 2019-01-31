## array();

To create a new array

```php
$number = array();
```

to put numbers in

```php
$number = array(4,2,2,2,3,6);
```

```php
echo $number[0];
echo $number[1];
...
```

or can put random string + number

```php
$mixed = array(3,4,"fix","this",9,"plz")
```

```php
echo $mixed[2];
echo $mixed[3];
```

> 4"fix"

or can even add array in array

```php
$random = array(3,4,array("x","y"))
```

```php
echo $random[2][0];
```

> "x"



To print the whole array (for debugging only)

```php
echo print_r($random)
```

> Array ( [0] => 3 [1] => 4 [2] => Array ( [0] => x [1] => y ) ) 1



if you want it look nicer:

```php
<pre>
    <?php echo print_r($random);
    ?>
</pre>
```

```
Array
(
    [0] => 3
    [1] => 4
    [2] => Array
        (
            [0] => x
            [1] => y
        )

)
1
```



To add to the end:

```php
$random[] = "new elemnt";
```




## array shortcut

can also do shortcut like

```php
$random = [0,1,2,3,4];
```



# Associative Arrays

Like dictionary, it has key-value pair.

```php
<?php
    $hero_list = array("name" => "Genji", "damage" = 999);
?>
```

When you want to call, can do

```php
<?php
    echo $hero_list["name"];
	echo "<br \>";
	echo $hero_list["damage"];
?>
```

>Genji
>
>999



If you want to do multiple, can do like

```php
<?php
    $hero_list = [
        array("name" => "Genji", "damage" => 9999),
        array("name" => "Sombra", "damage" => 20000),
        array("name" => "Hanzo", "damage" => 600),
    ];
?>
```

```php
<?php 
    for($i = 0; $i < count($hero_list); $i ++)
    {
        echo $hero_list[$i]["name"];
        echo "<br />";
        echo $hero_list[$i]["damage"];
        echo "<br />";
    }
?>
```

> Genji
>
>  9999
>
>  Sombra
>
>  20000
>
>  Hanzo
>
>  600

# ARRAY FUNCTION


## array length

```php
count($array);
```


## Max Value

```
max($array);
```

- Works with both String and Int array, not Associative array.

## Min value

```php
min($array);
```

- Works with both String and Int array, not Associative array.

## Sort

```php
sort($array);
```

- Works with all type of array including mixed, for associative array will sort the first attribute.

## Reverse sort

```php
rsort($array);
```

- Works with all type of array including mixed, for associative array will sort the first attribute.

## implode

Using implode you can read the array more naturally instead of using `print_r`

```php
$num_array = [1,2,3,4,90,110,-39,495,0];
echo implode(",",$num_array)
```

> 1,2,3,4,90,110,-39,495,0

## explode

to convert implode result to an array;

```php
$ok = implode(",",$num_array);
print_r explode(",",$ok);
```

> Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 4 [4] => 90 [5] => 110 [6] => -39 [7] => 495 [8] => 0 )

or can do with string

```php
$ok = "3,4,5,6,1,1,1,2,0";
print_r(explode(",",$ok));
```

> Array ( [0] => 3 [1] => 4 [2] => 5 [3] => 6 [4] => 1 [5] => 1 [6] => 1 [7] => 2 [8] => 0 )

## check if one item in the array

```php
in_array(3,$num_array);
```

> 1

```php
in_array(-1,$num_array);
```

> //nothing

Can do with string as well