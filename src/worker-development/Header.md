# Header
## 说明:
```php
void App::Header($header)
```

设置http响应头


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置实例的名称
$app->name = 'xtgxiso';

//注册路由/
$app->HandleFunc("/",function() {
     //自定义响应头
     $this->Header("server: xtgxiso");
     //以json格式响应
     $this->ServerJson(array("name"=>"WebWorker"));
});

Worker::runAll();

```
