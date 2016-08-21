##

##

There are three different types of visibility. Public, protected and private. You can define a property or a method with one of these visibilities. The effect is, how you can access the property or method. 
You should use public if need to access them from everywhere. Protected you can use from everywhere inside a class and even in the parents. Private is only allowed to access from the class object. 


```php

class Foo
{

   public $counter = 0;

   protected $multiplier;

   private $percent;


   public function setMultiplier($int)
   {
      $this->multiplier = $int;
   }


}

```
