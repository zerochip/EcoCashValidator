# numValidator

phone number verifier for zim networks.
the function has 2 parameters:

1. service provider - this can be the name of the network or its mobile payment system
 
 eg. econet or ecocash
2. the phone number to be verified

Like this:
```php
$object->isvalid(sp,phn).
//sp = service provider, phn = phone number
```

Example of use in code:
```php
$num = new NumValidator();

$sp = 'econet';
$phonum = $_POST['phonum'];

$num->isvalid($sp,$phonum);
```
This function returns a boolean ie **true** or **false**.

If **false** is returned the error will be stored in the property **numError**.

```php
$num->numError;
```