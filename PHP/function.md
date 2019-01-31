# function

```php
function name($arg1, $arg2) {
    statement;
}
```



## multiple return

```php
function add_subt($val1,$val2) {
    $add = $val1 + $val2;
    $subt = $val1 - $val2;
    return array($add, $subt);
}

list($add_result,$subt_result) = add_subt(10,5);

```

> `$add_result` = `$add`
>
> `$sub_result` = `$subt`

