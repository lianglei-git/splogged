1. 使用文件通信把...
   
branch process message --> send "10 bytes"

abc.log 1231231231, 下次写就是在这里

主进程可以写文件，子进程、工作线程 都可以写入文件，这点是没问题的
不仅要写入文件，并且还需要进行前端的通信，这里要用到ws，要把工作线程或者子进程的日志输出到前端。 
完全不清楚这到底是不是子进程或线程。。 这样怎么去输出到前端呢？ 
这个ws只能存在于主进程里面。

ws 单例模式






work:
stream -> logged -> ui -> server -> ui -> client
流输出     日志控制

    