# onAppStart
## 说明:
```php
callback App::$onAppStart
```

设置App启动时的回调函数，即当App启动后立即执行App::onAppStart成员指定的回调函数


## 回调函数的参数

``` $app ```

即App对象



## 范例


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

$app->onAppStart = function($app)
{
     echo "app starting...\n";
};

```

