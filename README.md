# push

## Introduction

Third party message push

## Install

```
$ composer require cutcop/push
```

## Demo

```php
<?php

require __DIR__ . '/vendor/autoload.php';

$appKey = 'your-app-key';
$masterSecret = 'your-master-secret';

$alert = 'Hi JPush!';
$extras = [
    'type' => 1,
    'url' => ''
];
$platform = ['android', 'ios'];
$audience = [
    'alias' => ['13888888888']
];

$push = new cutcop\Push\JPush($appKey, $masterSecret);
$push->push($alert, $extras, $platform, $audience);
```