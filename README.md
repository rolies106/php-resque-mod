# PHP Resqu

Resque is a Redis-backed library for creating background jobs, placing
those jobs on multiple queues, and processing them later.

This is fork project from [php-resque](https://github.com/chrisboulton/php-resque) by [chrisboulton](https://github.com/chrisboulton), for usage without composer and add phpredis as main Redis class and Credis as fallback.

## Background ##

Resque was pioneered and is developed by the fine folks at GitHub (yes,
I am a kiss-ass), and written in Ruby. What you're seeing here is an
almost direct port of the Resque worker and enqueue system to PHP.

For more information on Resque, visit the official GitHub project:
 <http://github.com/defunkt/resque/>

For further information, see the launch post on the GitHub blog:
 <http://github.com/blog/542-introducing-resque>

The PHP port does NOT include its own web interface for viewing queue
stats, as the data is stored in the exact same expected format as the
Ruby version of Resque.

The PHP port provides much the same features as the Ruby version:

* Workers can be distributed between multiple machines
* Includes support for priorities (queues)
* Resilient to memory leaks (fork)
* Expects failure

It also supports the following additional features:

* Has the ability to track the status of jobs
* Will mark a job as failed, if a forked child running a job does
not exit with a status code as 0
* Has built in support for `setUp` and `tearDown` methods, called
pre and post jobs

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
