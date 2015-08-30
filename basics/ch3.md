# PHP Tutorial: The Basics
# Chapter 3: Functions

## PHP Functions
There are many functions in PHP. You can visit [php.net](http://php.net) and checkout the documentation. 

In this tutorial I will use some functions you will have to use really often. 


### String Functions 

One important part are the `string functions`. These are functions to manipulate strings.

```php

$input = 'Hello World';

// get the length of a string 
strlen($input); // 11

// replace strings
str_replace('World', 'Toby', $input); // Hello Toby

// get a part of a string 
substr($input, 0, 5); // Hello

```
