# think-in-programming
programming: design, coding, framework

## 控制反转
* 概念：https://en.wikipedia.org/wiki/Inversion_of_control
* 要和**依赖反转**区分开
* 反转的是什么? 反转的是调用方向。传统的命令式的编程是，程序员写控制逻辑**调用**第三方库的一些功能；现代的方式是，程序员主要写的是业务逻辑函数，并把这个逻辑**注册**到第三方框架，第三方框架去真正**调用**程序员写的业务逻辑, 反转就发生在这个时候。
