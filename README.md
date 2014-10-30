# RFC 4122 UUID

The following class generates VALID RFC 4122 COMPLIANT
Universally Unique IDentifiers (UUID) version 3, 4 and 5.

UUIDs generated validates using OSSP UUID Tool, and output
for named-based UUIDs are exactly the same. This is a pure
PHP implementation.

Author: [Andrew Moore](https://github.com/FineWolf?)
posted this as a [note](http://www.php.net/manual/en/function.uniqid.php#94959) at the PHP Manual back in 2010.

## Install

If you're using [Composer](https://getcomposer.org/) as a package manager for PHP, put this require directive in your `composer.json` and run `composer install` in your CLI.

```json
{
  "require" : {
    "macx/rfc-4122-uuid" : "1.0.*"
  }
}
```

Or require via command line with: `composer require macx/rfc-4122-uuid 1.0.*`

## Generate a unique ID

To generate a ID simply copy the following code:

```php
include 'vendor/autoload.php';

$uuid = macx\UUID::v4();

echo 'The generated UUID is `' . $uuid . '`';
```

If you want to validate a ID against RFC do this:

```php
$givenId = 'f81d4fae-7dec-11d0-a765-00a0c91e6bf6';

if(macx\UUID::is_valid($givenId)) {
  // do something
}
```
