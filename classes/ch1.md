# PHP Tutorial: Classes
# Chapter 1: Object Oriented Programming


## Introduction


## Basics

```php
/**
 * Class User
 *
 * @author Tobias Maxham <git2016@maxham.de>
 */
class User // definition of the class User.
{
    // definition of the class attributes name, email and password.
    public $name;
    public $email;
    public $password;

    // definition of the method setEmail
    function setEmail($newEmail)
    {
        if (filter_var($newEmail, FILTER_VALIDATE_EMAIL) !== false) {
            $this->email = $newEmail;
            return true;
        }
        return false; // email could not be set. Invalid email.
    }
}

// create two new objects. John and Jane
$john = new User();
$john->name = 'John Doe';
$john->setEmail('john@doe.net');

$jane = new User();
$jane->name = 'Jane Doe';
$jane->setEmail('jane@doe.net');

echo 'Johns email is ' . $john->email . ' and Janes email is ' . $jane->email;
```