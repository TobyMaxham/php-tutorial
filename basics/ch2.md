# PHP Tutorial: The Basics
# Chapter 2: First steps


## Generall using
First of all you should know that it's possible to use *PHP-Code* between *HTML-Code*.

Create a **sample.php** file in your directory.

```php
<?php

echo "Hello World!";
```

To use it within your *HTML-Code* simple use


```php
<h1>This is the Headline</h1>

<?php
echo "Hello World!";
?>
```



###Schleifen:

Foreach:
```php

$apostles = ['Simon', 'Andrew', 'James'];

foreach($apostles as $apostle)
{
    echo $apostle . '<br />';
}

```

For:
```php

$apostles = ['John', 'Philip', 'Bartholomew', 'Thomas'];

for($i=0;$i<count($apostles);$i++)
{
  echo $apostles[$i] . '<br />';
}

```

While:
```php

$apostles = ['Matthew', 'Thaddaeus', 'Judas Iscariot'];

$i = 0;
while($i < count($apostles))
{
    echo $apostles[$i] . '<br />';
    $i++;
}

```

Do-While:
```php

$apostles = ['James', 'John', 'Philip', 'Bartholomew'];

$i = 0;
do
{
    echo $apostles[$i] . '<br />';
    $i++;
} while($i < count($apostles));

```

