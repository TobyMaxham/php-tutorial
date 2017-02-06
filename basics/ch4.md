# PHP Tutorial: The Basics
# Chapter 4: JSON

## JavaScript Object Notation
"JSON is a language-independent data format. It derives from JavaScript, but as of 2016 many
programming languages include code to generate and parse JSON-format data.
The official Internet media type for JSON is application/json.
JSON filenames use the extension `.json`." [From Wikipedia](https://en.wikipedia.org/wiki/JSON)


### Decoding a JSON string


The `json_decode()` function takes a JSON-encoded string as its first parameter and parses it into a PHP variable.<br>

Normally, `json_decode()` will return an **object of** [\stdClass](http://php.net/manual/en/reserved.classes.php)
if the top level item in the JSON object is a dictionary or an **indexed array** if the
JSON object is an array. It will also return scalar values or `NULL` for certain scalar values,
such as simple strings, `"true"`, `"false"`, and `"null"`. It also returns `NULL` on any error.


```php

// Returns an object (The top level item in the JSON string is a JSON dictionary)
$json_string = '{"name": "Toby", "age": 27, "active": true, "skills": ["php", "sql", "json"]}';
$object = json_decode($json_string);
printf('Hello %s, You are %s years old.', $object->name, $object->age);
#> Hello Toby, You are 27 years old.


// Returns an array (The top level item in the JSON string is a JSON array)
$json_string = '["Toby", 27, true, ["php", "sql", "json"]]';
$array = json_decode($json_string);
printf('Hello %s, You are %s years old.', $array[0], $array[1]);

```
