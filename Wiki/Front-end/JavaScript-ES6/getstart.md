

## 两种注释方法

```js
// 单行注释

var city='nanjing' // variable 声明

/*
多行注释
*/
```


## 常量（constants）
- const：只读常量
    - 常量名一般会大写

## 变量

### 变量名（标识符）规范

1. 区分大小写；
2. 字母、_、$ 这三种符号为开头；
3. 推荐使用 Python 的命名规范，而不是使用 Java 的大驼峰命名规范；

### 声明变量

- var：全局变量
    - 一定要声明，避免直接使用 x=100 这种形式
- let：局部变量
    - 详见函数作用域


### 变量赋值

- 使用变量前，一定要声明（废话，不声明咋使用），不然会引起引用错误（ReferenceError）；
- 如果一个变量在声明的时候没有赋值，那么这个变量值就是 `undefined`；



