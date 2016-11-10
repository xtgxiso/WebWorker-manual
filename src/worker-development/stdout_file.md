# stdoutFile
## 说明:
```php
static string App::$stdoutFile
```

此属性为全局静态属性，如果以守护进程方式(```-d```启动)运行，则所有向终端的输出(echo var_dump等)都会被重定向到stdoutFile指定的文件中。

如果不设置，并且是以守护进程方式运行，则所有终端输出全部重定向到```/dev/null```


