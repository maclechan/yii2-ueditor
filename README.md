Yii2 Ueditor
Yii2 - 百度编辑器
==============

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
composer require --prefer-dist maclechan/yii2-ueditor "*"
```

or add

```
"maclechan/yii2-ueditor": "*"
```

to the require section of your `composer.json` file.

then add

```
'maclechan\\ueditor\\' => array($vendorDir . '/maclechan/yii2-ueditor'),
```

to the return array of your `composer/autoload_psr4.php` file


notes: all of the files in the `vendor/maclechan/yii2-ueditor/` 

Usage
-----

Once the extension is installed, simply use it in your code by  :

view
```php

<?php
use maclechan\ueditor\Ueditor;
echo UEditor::widget([
	'id'=>"Test[content]",
    'events' => [
        //编辑区域大小
        //'initialFrameHeight' => '4800',
        //设置语言
        'lang' =>'en', //中文为 zh-cn
        //定制菜单
        'toolbars' => [
            [
                'fullscreen', 'source', 'undo', 'redo', '|',
                'fontsize',
                'bold', 'italic', 'underline', 'fontborder', 'strikethrough', 'removeformat',
                'formatmatch', 'autotypeset', 'blockquote', 'pasteplain', '|',
                'forecolor', 'backcolor', '|',
                'lineheight', '|',
                'indent', '|'
            ],
        ],
        
    ],
    'ucontent'=>$model->content,
]);

?>

or
<?= $form->field($model, 'content')->widget('maclechan\ueditor\Ueditor',['id'=>'Test[content]']); ?>
//在编辑时，显示默认值
<?= $form->field($model, 'content')->widget('maclechan\ueditor\Ueditor',['id'=>'Test[content]','ucontent'=>$model->content])->label(false); ?>
```


email  maclechanchan@qq.com
qq     429140141