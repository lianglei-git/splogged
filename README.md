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

    

2022/12/29
做架构的前提一定是开发公用的软硬件。供他人使用，并且有大量的测试脚本，更要熟悉低级语言实现高级语言的过程；

查看大型项目设计，承载这些大型项目的设计，甚至计算机的设计等；

