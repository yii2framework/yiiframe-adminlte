Yii2 AdminLTE Asset Bundle
=======================
Adminlte Background Administration framework resource file for yiiframe

[![Latest Stable Version](http://poser.pugx.org/yii2framework/yiiframe-adminlte/v)](https://packagist.org/packages/yii2framework/yiiframe-adminlte) [![Total Downloads](http://poser.pugx.org/yii2framework/yiiframe-adminlte/downloads)](https://packagist.org/packages/yii2framework/yiiframe-adminlte) [![Latest Unstable Version](http://poser.pugx.org/yii2framework/yiiframe-adminlte/v/unstable)](https://packagist.org/packages/yii2framework/yiiframe-adminlte) [![License](http://poser.pugx.org/yii2framework/yiiframe-adminlte/license)](https://packagist.org/packages/yii2framework/yiiframe-adminlte) [![PHP Version Require](http://poser.pugx.org/yii2framework/yiiframe-adminlte/require/php)](https://packagist.org/packages/yii2framework/yiiframe-adminlte)

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist yii2framework/yiiframe-adminlte "*"
```

or add

```
"yii2framework/yiiframe-adminlte": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
use yiiframe\adminlte\AdminLetAsset;
class AppAsset extends AssetBundle
{
    public $basePath = '@webroot';
    public $baseUrl = '@web/resources';

    public $css = [
        'plugins/toastr/toastr.min.css', // 状态通知
        'plugins/fancybox/jquery.fancybox.min.css', // 图片查看
        'plugins/cropper/cropper.min.css',
        'css/yiiframe.css',
        'css/yiiframe.widgets.css',
    ];

    public $js = [
        'plugins/layer/layer.js',
        'plugins/sweetalert/sweetalert.min.js',
        'plugins/fancybox/jquery.fancybox.min.js',
        'js/template.js',
        'js/yiiframe.js',
        'js/yiiframe.widgets.js',
    ];

    public $depends = [
        YiiAsset::class,
        AdminLetAsset::class,
        HeadJsAsset::class
    ];
}
```