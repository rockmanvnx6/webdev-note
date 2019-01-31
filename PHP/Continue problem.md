# Continue

```php
for ($count = 0; $count <= 10; $count ++) {
    if ($count == 5) {
        continue;
    }
    echo $count .", ";
}
```

> 0, 1, 2, 3, 4, 6, 7, 8, 9, 10,



However if we do with while loop

```php
 while($count <= 10) {
        if($count == 5) {
            continue;
        }
        echo $count .", ";
        $count ++;
 }
```

The problem with this is that if we do continue, it will skip the whole while loop and start from the beginning again. Thus the `$count ++` will never be executed.

In for loop, since the increment is built-in, it's ok.



## continue argument

```php
for($i = 0; $i<=5; $i ++) {
    for ($k = 0; $k <= 5; $k ++) {
        if($k == 2) {
            continue(2);
        }
        echo "{$i}-{$k} <br/>";
    }
}
```

> continue(2) means continue 2 loop before it.
>
> continue in default is continue(1) which only skip the current loop.

Result:

0-0

0-1  

1-0  

1-1 

2-0  

2-1  

3-0  

3-1  

4-0  

4-1  

5-0  

5-1 



> Break can be used the same as well: break(1), break(2);