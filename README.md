# Simple notification widget for Yii2

[![SymfonyInsight](https://insight.symfony.com/projects/056b7d4e-da1d-42bd-9f18-9381ffa7ad85/mini.svg)](https://insight.symfony.com/projects/056b7d4e-da1d-42bd-9f18-9381ffa7ad85)

Noty widget for Yii2

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require dominus77/yii2-noty
```

or add

```
"dominus77/yii2-noty": "^1.0"
```

to the require section of your `composer.json` file.


## Usage

Once the extension is installed, simply use it in your layout file like this:

Controller:
```php
<?php
// ...
Yii::$app->session->setFlash(\dominus77\noty\NotyWidget::TYPE_SUCCESS, 'Hello World!');
// ...

```

View:
```php
<?php
use dominus77\noty\NotyWidget;
?>

<?= NotyWidget::widget([
    'typeOptions' => [
        'success' => ['timeout' => 3000],
        'info' => ['timeout' => 3000],
    ],
    'options' => [
        'progressBar' => true,
        'timeout' => false,
        'layout' => 'topCenter',
        'dismissQueue' => true,
        'theme' => NotyWidget::THEME_SUNSET
    ],
]) ?>
```
## More Information
Please, check the [Noty](https://ned.im/noty/#/about)

## Testing
```
$ phpunit
```

## License
The MIT License (MIT). Please see [License File](https://github.com/Dominus77/yii2-noty/blob/master/LICENSE.md) for more information.

## SymfonyInsight
[![SymfonyInsight](https://insight.symfony.com/projects/056b7d4e-da1d-42bd-9f18-9381ffa7ad85/big.svg)](https://insight.symfony.com/projects/056b7d4e-da1d-42bd-9f18-9381ffa7ad85)