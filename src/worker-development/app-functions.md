# App类
WebWorker中有一个重要的类App。

App类用于实现端口的监听，并可以设置客户端连接事件、连接上消息事件、连接断开事件的回调函数，从而实现业务处理。

可以设置app实例的进程数（count属性），app主进程会fork出count个子进程同时监听相同的端口，并行的接收客户端连接，处理连接上的事件。