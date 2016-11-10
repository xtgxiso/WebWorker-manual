# daemonize
## 说明:
```php
static bool App::$daemonize
```

此属性为全局静态属性，表示是否以daemon(守护进程)方式运行。如果启动命令使用了 ```-d```参数，则该属性会自动设置为true。也可以代码中手动设置。


