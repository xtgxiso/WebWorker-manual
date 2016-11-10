# count

## 说明:
```php
int App::$count
```

设置当前app实例启动多少个进程，不设置时默认为1。


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置进程数为4
$app->count = 4;

```
