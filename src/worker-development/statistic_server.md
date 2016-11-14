# statistic_server

## 说明:
```php
string App::$statistic_server
```

设置监控服务(workerman-statistics)的地址,默认不监控服务，如设置请确保workerman-statistics已经启动。


## 范例

```php

$app = new WebWorker\App("http://0.0.0.0:1215");

//设置监控地址
$app->statistic_server = "udp://127.0.0.1:55656";

```
