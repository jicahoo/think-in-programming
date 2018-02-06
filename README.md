# think-in-programming
programming: design, coding, framework

## 控制反转
* 概念：https://en.wikipedia.org/wiki/Inversion_of_control
* 要和**依赖反转**区分开
* 反转的是什么? 反转的是调用方向。简单讲，原来是业务代码调用库，现在是库调用业务代码。传统的命令式的编程是，程序员写控制逻辑**调用**第三方库的一些功能；现代的方式是，程序员主要写的是业务逻辑函数，并把这个逻辑**注册**到第三方框架，第三方框架去真正**调用**程序员写的业务逻辑, 反转就发生在这个时候。
* 例子:
```java
List<String> words = Arrays.asList( "the", "quick", "brown", "fox", "jumped", "over", "the", "lazy", "dog");

//控制反转之前, 循环逻辑是由程序员写出来的。
for(String word : words) {
  System.out.println(word);
}

//(RxJava)控制反转之后，循环逻辑是有RxJava框架写的，程序员写出的代码只是将这个打印函数告诉框架。
Observable.from(words)
          .subscribe(word->System.out.println(word));
```
