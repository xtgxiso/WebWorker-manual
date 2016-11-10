# HandleFunc
## 说明:
```php
void App::HandleFunc($url,callable $callback)
```

注册路由，当访问的路径和url完全匹配的时候，则会执行$callback，访问的时候兼容有无“/”线. 如注册的是"/test",则"/test"和"/test/"均可以访问,可以重复注册，默认的执行顺序即为注册的顺序，如果想在其中一个退出，不想执行下面的注册，只要在其中的路由中返回true即可


## 函数的参数

``` $url ```

注册的url

``` $callback ```

url对应要执行的代码



## 范例一注册路由


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//注册路由hello
$app->HandleFunc("/hello",function() use($app){
    $app->server_send("Hello World WorkerMan WebWorker!");
});


```



## 范例二重复注册路由，则按注册顺序执行


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//注册路由hello
$app->HandleFunc("/hello",function() use($app){
    $app->txt = time()."hello-1";
});

//注册路由hello
$app->HandleFunc("/hello",function() use($app){
    $app->txt .= "<br/>hello-2";
    $app->server_send($app->txt);
});


```



## 范例三重复注册路由，符合条件则中断路,否则继续执行


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//注册路由hello
$app->HandleFunc("/hello",function() use($app){
    if ( rand(1,10) > 5 ){
	$app->server_send("中断路由");
	return true;
    }
});

//注册路由hello
$app->HandleFunc("/hello",function() use($app){
    $app->server_send($app->server_send("路由执行到最后"));
});


```



