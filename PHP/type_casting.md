# settype($var, type)

or

```php
$var = (type)$var
```



type list

 - string
- int , "integer"
- array
- float
- bool, "boolean"

**Example**

```php
<?php
    $var = "1,23,4,56,5";
    $var = (array)$var;
    print_r($var);
?
```

> Array ( [0] => 1,23,4,56,5 )

# to check type

```php
gettype($var)
```

