


```php
<?php

class Foo
{

   /**
   *@var Bar
   */
   private $bar;

   function __construct(Bar $bar)
   {
      $this->bar = $bar;
   }

   public static function getBar()
   {
   }

}

```
