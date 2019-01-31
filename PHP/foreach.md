# foreach

```php
foreach ($array as $value)
    statement;
```



**Example**

```php
<?php
    $ages = array(4,8,15,16,23,42);

    foreach($ages as $age) {
        echo "Age: {$age}<br /> ";
    }
?>
```

>Age: 4 Age: 8 Age: 15 Age: 16 Age: 23 Age: 42



## For each for associative array

```php
foreach ($array as $key => $value) {
    statement;
}
```



**Example**

```php
$hero = array(
    "name" => "Genji",
    "damage" => 999,
    "skills" => 4,
    "ulti-ready" => "false"
);

foreach($hero as $key => $value) {
    $key = ucfirst($key);
    echo "{$key}: {$value}<br />";
}
```



> Name: Genji 
>
> Damage: 999 
>
> Skills: 4
>
> Ulti-ready: false

