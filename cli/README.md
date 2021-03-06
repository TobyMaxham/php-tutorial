# Command Line Tool


Typically you would use PHP to build web-based applications. But you also could use it as a command line tool. 

First we create a new file `command` (without .php):

```php
#!/usr/bin/env php
<?php

// Check for console interface
if (php_sapi_name() != 'cli') exit(0);

// Make some input
fwrite(STDOUT, "Please enter your namen:\n");

// Read the input
$name = fgets(STDIN);

if (isset($_SERVER['argv'][1])) {
	$state = $_SERVER['argv'][1];
	if (strpos($state, 'morning') !== FALSE)
		$eOut = 'Good morning ';

	elseif (strpos($state, 'evening') !== FALSE)
		$eOut = 'Good evening ';

	elseif (strpos($state, 'night') !== FALSE)
		$eOut = 'Good night ';

	else $eOut = 'Hello ';
}

// Write to console
fwrite(STDOUT, $eOut . trim($name) . '.');

// Exit correctly
exit(0);
```

Try out:
```sh
php command
php command --morning
php command --evening
php command --night
```
