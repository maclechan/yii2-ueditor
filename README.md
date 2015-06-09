Yii2 Ueditor
Yii2 - 百度编辑器
==============

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
composer require --prefer-dist macle/yii2-ueditor "*"
```

or add

```
"macle/yii2-ueditor": "*"
```

to the require section of your `composer.json` file.

then add

```
'macle\\ueditor\\' => array($vendorDir . '/macle/yii2-ueditor'),
```

to the return array of your `composer/autoload_psr4.php` file


notes: all of the files in the `vendor/macle/yii2-ueditor/` 

Usage
-----

Once the extension is installed, simply use it in your code by  :

view
```php

<?php
use macle\ueditor\Ueditor;

echo Ueditor::widget(['id'=>"Test[desc]"]); 

?>

or
<?= $form->field($model, 'desc')->widget('macle\ueditor\Ueditor',['id'=>'Test[desc]']); ?>

```
