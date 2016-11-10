# Mredis 

## 说明:
```php
Mredis:getInstance:(array $config)
```

获取一个redis实例，根据参数已经进行了单例模式，相同的参数只会连接一次,由于该继承原生的redis类，所以该类的用法和原生的是一样的。



##函数的参数

``` $config ```

即redis连接参数,支持如下关键key

host对应redis主机

port对应redis端口

password对应redis密码

db对应redis连接的库     		     




## 范例


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

$config = array();
$config["redis"]["host"] = "127.0.0.1";
$config["redis"]["port"] = 6379;
$config["redis"]["password"] = "123456";
$config["redis"]["db"] = 1;

//获取redis的值
$app->HandleFunc("/",function() use($app,$config){
     $redis = Mredis::getInstance($config["redis"]);
     $app->server_send($redis->get("xtgxiso"));
});



```

