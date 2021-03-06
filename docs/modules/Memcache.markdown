---
layout: doc
title: Codeception - Documentation
---

# Memcache Module

Connects to [memcached](http://www.memcached.org/) using either _Memcache_ or _Memcached_ exitnsion.

Performs a cleanup by flushing all values after each test run.

### Configuration

* host: localhost - memcached host to connect
* port: 11211 - default memcached port.

Be sure you don't use the production server to connect.

### Public Properties

* memcache - instance of Memcache object


### Actions


#### clearMemcache


Flushes all Memcached data.


#### dontSeeInMemcached


Checks item in Memcached doesn't exist or is the same as expected.

 * param $key
 * param bool $value


#### grabValueFromMemcached


Grabs value from memcached by key

Example:

{% highlight php %}

<?php
$users_count = $I->grabValueFromMemcached('users_count');
?>

{% endhighlight %}

 * param $key
 * return array|string


#### seeInMemcached


Checks item in Memcached exists and the same as expected.

 * param $key
 * param $value
