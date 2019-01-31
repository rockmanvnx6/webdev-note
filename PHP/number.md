## Absolute value

```php
<?php 
    echo abs(3-300)
?>
```

## Exponential

```php
<?php
    echo pow(2,8);
?>
```

## Square root

```php
<?php
    echo sqrt(100);
?>
```

## Modulo

```php
<?php
    echo fmod(20,7);
?>
```

> modulo. = 20%7;

## Random

```php
<?php
    echo rand();
?>
```

## random (min,max)

```php
<?php
    echo rand(1,10);
?>
```



In php `"1 houses" + 1 = 2;`

## round(number, decimal place)

```php
<?php
    round(4.555,2);
?>
```

> 4.56

## ceil(number) - round up

```php
<?php
    ceil(4.3);
?>
```

> 5

## floor(number) - round down

```php
<?php
    floor(4.8)
?>
```

> 4



## is_int(number) - check if the number is integer

```php
<?php
   echo is_int(4);
?>
```

> 1

```php
<?php
    echo is_int(4.5);
?>
```

> //return nothing

## is_float(number)

```php
<?php
    echo is_float();
?>
```

return like is_int

## is_numeric(number)

```php
<?php
    echo is_numberic();
?>
```

return like is_int