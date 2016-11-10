# user

## 说明:
```php
string App::$user
```

设置当前App实例以哪个用户运行。此属性只有当前用户为root时才能生效。不设置时默认以当前用户运行。

建议```$user```设置权限较低的用户，例如www-data、apache、nobody等。



## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置以用户xtgxiso运行
$app->user = 'xtgxiso';

```
