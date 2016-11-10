# autoload

## 说明:
```php
array App::$autoload 
```

设置自动加载的目录,会加载目录下的所有php文件(仅一级不支持递归)。


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置自动加载
$app->autoload = array(__DIR__."/controllers/",__DIR__."/libs/",__DIR__."/funcs/",__DIR__."/models/");

```
