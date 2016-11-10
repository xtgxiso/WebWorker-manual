# 目录结构
<pre>
WebWorker
    Applications                  // 应用目录，存放所有的应用
        ├── Demo1                 // 演示 demo1应用 相关
        │   ├── config            // 配置目录
        │   ├── controllers       // 控制器目录
        │   ├── funcs             // 存放函数目录
        │   ├── libs              // 存放类目录
        │   ├── models            // 存放数据模型目录
        │   └── start.php         // demo1应用入口文件
    WebWorker                     // webworker框架目录
        ├── Libs                  // 存放框架类
        │     ├── Mdb.php         // 用于实例化Mmysqli类
        │     ├── Mmysqli.php     // mysqli类封装
        │     ├── Mredis.php      // redis类封装
        ├── App.php               // 框架核心
    Statistics                    // 监控应用目录
    benchmark                     // 性能测试目录相关
    workerman-for-win             // workerman的win版本
    workerman                     // workerman的linux版本
    start.php                     // 所有应用总入口
</pre>
