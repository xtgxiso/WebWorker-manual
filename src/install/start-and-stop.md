# 启动与停止

注意WebWorker启动停止等命令都是在命令行中完成的。

要启动WebWorker，首先需要有一个启动入口文件，里面定义了服务监听的端口及协议。可以参考[入门指引--简单开发实例部分](/getting-started/simple-example.html)


这里以[demo](https://github.com/xtgxiso/WebWorker)为例，它的启动入口为start.php。
### 启动

以debug（调试）方式启动

```php start.php start```

以daemon（守护进程）方式启动

```php start.php start -d```

### 停止
```php start.php stop```


### 查看状态
```php start.php status```







