# PHP Tutorial: Classes
# Chapter 4: Static Classes


```php
// Foo.php

class Foo
{

    /**
     * @var Foo $foo
     */
    private static $foo;

    function __construct()
    {
        self::$foo = new self();
    }

    /**
     * @return Foo
     */
    public static function getFoo()
    {
        return self::$foo;
    }
}
```

```php
// test.php

Foo::getFoo();

```
