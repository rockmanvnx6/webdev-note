# Scope

```php
$a = "outside";
function change() {
	$a = "inside";    
}
change();
echo $a;
```

> outside



even if

```php
$a = "outside";
function change($a) {
    $a = "inside";
}
change($a);
echo $a;
```

> outside



to fix:

```php
$a = "outside";
function change() {
    global $a;
    $a = "inside";
}
change();
echo $a;
```

