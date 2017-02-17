# Setcookie
## 说明:
```php
void App::Setcookie($name,$value = '',$maxage = 0,$path = '',$domain = '',$secure = false,$HTTPOnly = false)
```

设置cookie


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置实例的名称
$app->name = 'xtgxiso';

//注册路由/
$app->HandleFunc("/",function() {
     //设置cookie
     $this->Setcookie("xtgxiso",time()); 
     //以json格式响应
     $this->ServerJson(array("name"=>"WebWorker"));
});

Worker::runAll();

```
