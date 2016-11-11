# AddFunc
## 说明:
```php
void App::AddFunc($url,callable $callback)
```

注册中间件，当注册的的url是访问url路由前缀的一部时候，则会执行$callback.比如 如注册的是"/api",则访问"/api/user"或"/api/news"均会执行"/api"的中间件.路由注册和中间件注册的执行顺序取决于注册顺序


## 函数的参数

``` $url ```

注册的url

``` $callback ```

url对应要执行的代码



## 范例一应用级中间件


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//应用级中间件--对所有访问启用ip限制访问
$app->AddFunc("/",function() use($app){
    if ( $_SERVER['REMOTE_ADDR'] != '127.0.0.1' ) {
        $app->ServerHtml("禁止访问");
        return true;//返回ture,中断执行后面的路由或中间件，直接返回给浏览器
    }   
});

//注册路由
$app->HandleFunc("/",function() use($app){
    $app->ServerHtml("Hello World");
});


//注册路由hello
$app->HandleFunc("/xtgxiso",function() use($app){
    $app->ServerHtml("xtgxiso");
});


```




