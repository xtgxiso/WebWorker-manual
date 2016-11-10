# 序言

[PHP](http://www.php.net)是一种被广泛应用的开源脚本语言，绝大多数开发者使用PHP做基于Web的应用程序，并且有了很多非常知名的Web框架，如laravel、Yii、slim等。

传统的PHP应用程序基本上是apache+mod_php或nginx+fpm中运行的，PHP本身不处理HTTP协议(虽然有php -s但无法生产用)，那么PHP能不能脱离apache或nginx来独立提供http服务呢?这时候WebWorker就是你的最佳选择。

WebWorker是一款纯PHP开发的开源的高性能的PHP http服务器框架（基于WorkerMan框架），用于开发高性能的api应用，例如app接口服务端等。




