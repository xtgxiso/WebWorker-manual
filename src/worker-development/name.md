# name

## 说明:
```php
string App::$name
```

设置当前App实例的名称，方便运行status命令时识别进程。不设置时默认为none。


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置实例的名称
$app->name = 'xtgxiso';

```

