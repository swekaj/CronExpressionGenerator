CronExpressionGenerator
=======================

Generate valid, random cron expressions.


Installation
------------

Add the CronExpressionGenerator library to your `composer.json` file:

    composer require swekaj/cron-expression-generator

Usage
-----

To  use this with [Faker](https://github.com/fzaninotto/Faker), you must add the `CronExpressionGenerator\FakerProvider` class to the Faker generator:

```php
<?php

$faker = \Faker\Factory::create();
$faker->addProvider(new \CronExpressionGenerator\FakerProvider($faker));

// Generator                 sample output
$faker->cron();           // 12-38 */4 * * 2000/5
$faker->cronMinute();     // */12,30-39
$faker->cronHour();       // 0-23
$faker->cronDayOfMonth(); // L,14W,30
$faker->cronMonth();      // 1/2,6-8
$faker->cronDayOfWeek();  // 0-2,4W,3#2
$faker->cronYear();       // 2012,2000-2039
```
