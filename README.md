# PHP Resque

Resque is a Redis-backed library for creating background jobs, placing
those jobs on multiple queues, and processing them later.

This is fork project from [php-resque](https://github.com/chrisboulton/php-resque) by [chrisboulton](https://github.com/chrisboulton), for usage without composer and add phpredis as main Redis class and Credis as fallback.

## Requirements ##

* PHP 5.3+
* Redis 2.2+
* [phpredis](https://github.com/nicolasff/phpredis) for better performance

## Getting Started ##

```php
    require_once 'lib/ResqueAutoloader';
    ResqueAutoloader::register();

    // Run all Resque classes command
```

## More Info ##

You can see more information at [php-resque](https://github.com/chrisboulton/php-resque).
