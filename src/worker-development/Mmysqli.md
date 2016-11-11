#Mmysqli 

mysql的操作类,该类继承原生的mysqli，同时处理了自动重连机制，但在开发中请不要直接实例化该类，应该用Mdb::getInstance($config)来获取。



#Mdb

## 说明:
```php
Mdb:getInstance:(array $config)
```

获取一个mysqli实例，根据参数已经进行了单例模式，相同的参数只会连接一次。



##函数的参数

``` $config ```

即mysql连接参数,支持如下关键key

host对应mysql主机

user对应mysql用户

password对应mysql密码

db对应mysql连接的库

charset对应mysql的字符集     		     




## 范例


```php

$app = new WebWorker\App("http://0.0.0.0:1215");

$config = array();
$config["db"]["host"] = "127.0.0.1";
$config["db"]["user"] = "root";
$config["db"]["password"] = "123456";
$config["db"]["db"] = "test";
$config["db"]["port"] = 3306;
$config["db"]["charset"] = "utf8";

//获取mysql的值
$app->HandleFunc("/",function() use($app,$config){
    $db = Mdb::getInstance($config["db"]);
    $list = $db->query("select * from test")->fetch_all(MYSQLI_ASSOC);
    $app->ServerJson($list);
});



```

