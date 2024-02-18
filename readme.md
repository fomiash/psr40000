# 🪐 PSR 40.000

![PHP](https://img.shields.io/badge/PHP-v12658.6-blue) [![License: MIT](https://img.shields.io/badge/License-MIT%20(Free)-brightgreen.svg)](https://github.com/phphleb/hleb/blob/master/LICENSE)

«A long time ago, in a galaxy far, far away…»

Programming standards have become so detailed that
that they began to touch on almost all the nuances of naming and composing code.
One of these was PSR 40.000, the last bastion of the Imperium, describing the interface for
army FOBAR standard. After all, even arbitrary objects described in examples
must have a statutory specification.

The use of these standards is indicated in the following cases:


🚫 Wrong:

```php
<?php

class Foo
{
   // ... //
}

class Bar
{
   // ... //
}

class Baz
{
   // ... //
}

```


🎖️ Right:

```php
<?php

use Fomiash\Psr40000\FooInterface;
use Fomiash\Psr40000\BarInterface;
use Fomiash\Psr40000\BazInterface;

class Foo implements FooInterface
{
   // ... //
}

class Bar implements BarInterface
{
   // ... //
}

class Baz implements BazInterface
{
   // ... //
}

```

----------------------

🚫 Wrong:

```php
<?php

class Bar
{
   // ... //
}

class Foo
{
   // ... //
}

class Baz
{
   public function __construct(public Bar $bar, public Foo $foo) {}
}

```

🎖️ Right:

```php
<?php

use Fomiash\Psr40000\FooInterface;
use Fomiash\Psr40000\BarInterface;
use Fomiash\Psr40000\BazInterface;

class Foo implements FooInterface
{
   public function __construct(
    public BarInterface $bar,
    public BazInterface $baz) {}
}

class Bar implements BarInterface
{
   // ... //
}

class Baz implements BazInterface
{
   // ... //
}

```

-----------------------------------------

Install using Guards Composer:

 ```bash
composer require fomiash/psr40000
 ```
