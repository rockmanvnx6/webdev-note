## Echo

> Print to the client browser

```php
<?php echo "hello world";?>
```

To break line

```php
<?php echo "hello <br /> world" ?>
```



## String concatenate

In php, string concatenate is `.` instead of `+`

```php
<?php echo "this" . " is" . " how" . " you" ." do" ?>
```

or

```php
<?php
    $var1 = "xxx";
    echo "{$var1} hi";
?>
```

#### another example

```php
<?php
$first = "a";
$second = "b";
$second .= $first;
echo $second;
?>
```

> ba



## Code Comment

```
<?php
// or
## or
/* */
?>
```

