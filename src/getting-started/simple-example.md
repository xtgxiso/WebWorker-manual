# 简单的开发实例

## 实例一、使用HTTP协议对外提供服务
**创建http_test.php文件**
```php
<?php
use Workerman\Worker;
use Workerman\Protocols\Http;

require_once 'vendor/autoload.php';

$app = new WebWorker\App("http://0.0.0.0:1215");

//进程数
$app->count = 4;

//自动加载目录--会加载目录下的所有php文件
$app->autoload = array();

//注册路由
$app->HandleFunc("/",function() use($app){
    $app->ServerHtml("Hello World");
});

//自定义404
$app->on404  = function() use($app){
    $app->ServerHtml("我的404");
};

// 如果不是在根目录启动，则运行runAll方法
if(!defined('GLOBAL_START'))
{
    Worker::runAll();
}

// 运动 worker
Worker::runAll();

```

**命令行运行**
```shell
php http_test.php start

```

**测试**


假设服务端ip为127.0.0.1

在浏览器中访问url http://127.0.0.1:1215

