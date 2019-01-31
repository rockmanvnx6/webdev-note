# Short-open tags

Instead of

```php
<?php something ?>
```

Can do

```php
<? something ?>
```

```php
<?= something ?>
```

Different:

if using

```php
<?php 1+1;?> or <?php 1+1; ?>
```

the calculation will be calculated **in the server side**. 

However if we use :

```php
<?= 1+1; ?>
```

The website will display **2**.

> **White space** doesn't matter

