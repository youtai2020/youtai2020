# IO 编程

IO编程：input/output，就是输出和输入编程

程序和运行程序时数据是在内存中驻留的，由 CPU 执行，涉及到数据交换的地方一般是磁盘、网络等，这就需要 IO 接口；

IO 编程中， Stream（流），是一个重要的概念，类似数据就是水管的水，只能单向流动，要不然是 input，要不是 output ，input 就是数据流入水管，output 就是数据流出水管，一般客户端和浏览器就需要两个水管，发出数据和接受数据；

由于 CPU 和内存处理速度很快，外部设备（磁盘）速度跟不上，所以存在速度不匹配的问题，比如把 100M 数据处理，CPU 需要 0.01 秒，而磁盘需要 10 秒，这就带来了速度不匹配；

## 同步 IO

CPU 处理完数据，等待磁盘处理处理，等磁盘处理完数据，CPU 再继续执行程序，这里 CPU 需要等待程序执行完成，会造成资源的浪费；

## 异步 IO

CPU 处理完数据，交给磁盘，再去执行其他任务，也就是继续执行其他代码，等待磁盘告诉 CPU 执行完成，CPU 再回来继续执行下一步操作，这样子就是异步 IO，异步处理不会浪费资源，也就是性能会很好，但是比较复杂；

## 回调和轮询

这里就牵扯到一个复杂性问题，

**回调**：磁盘处理完数据，通知 CPU 执行完成，这个过程就是**回调**

**轮询**：CPU 随时检查磁盘处理结果，等磁盘处理完成，自动进行下一步操作
