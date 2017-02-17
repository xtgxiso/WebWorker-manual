# max_request

## 说明:
```php
int App::$max_request
```

设置当前app实例中每个进程处理多少请求后重启，主要目的是防止写的程序有问题导致内存泄露,不设置时默认为10000.


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置为0则表示不自动重启
$app->max_request = 0;

```
