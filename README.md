Yii2 AdminLTE Asset Bundle
=======================
Adminlte Background Administration framework resource file for yiiframe

[![Latest Stable Version](http://poser.pugx.org/hjp1011/yii2-adminlte/v)](https://packagist.org/packages/hjp1011/yii2-adminlte) [![Total Downloads](http://poser.pugx.org/hjp1011/yii2-adminlte/downloads)](https://packagist.org/packages/hjp1011/yii2-adminlte) [![Latest Unstable Version](http://poser.pugx.org/hjp1011/yii2-adminlte/v/unstable)](https://packagist.org/packages/hjp1011/yii2-adminlte) [![License](http://poser.pugx.org/hjp1011/yii2-adminlte/license)](https://packagist.org/packages/hjp1011/yii2-adminlte) [![PHP Version Require](http://poser.pugx.org/hjp1011/yii2-adminlte/require/php)](https://packagist.org/packages/hjp1011/yii2-adminlte)

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist hjp1011/yii2-adminlte "*"
```

or add

```
"hjp1011/yii2-adminlte": "*"
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