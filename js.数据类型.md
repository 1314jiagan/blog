## js数据类型
7种
* 数字 number
* 字符串 string
* 布尔 bool
* 符号 symbol
* 空 undefined
* 空 null
* 对象 object
  
数组、函数、日期它们都属于 object ，不是数据类型
## 数字
特殊值
正0 和 负0 都等于 0，要严谨

无穷大
Infinity 、+Infinity 、-Infinity

无法表示的数字
NaN (Not a Number)
但它是一个数字
## 字符串
* 单引号
'你好'
* 双引号
"你好"
* 反引号
``` `你好` ```

注意
引号不属于字符串的一部分，就像书名号不属于书名的一部分一样

如果要在单引号里面包含单引号怎么办？
```
'it\'s ok'
"it's ok"
`it's ok`
```
### 转义
```
\' 表示 '
\" 表示 "
\n 表示换行
\r 表示回车
\t 表示 tab 制表符
\\ 表示 \
\uFFFF 表示对应的 Unicode 字符
\xFF 表示前 256 个 Unicode 字符
```
### 字符串长度
```
'123'.length // 3
'\n\r\t'.length // 3
''.length // 0
' '.length // 1
```
### 通过下标来读取字符
```
let s = 'hello';
s[0] // "h"
```
## 布尔
五个 falsy 值
falsy 就是相当于 false 但又不是 false 的值
分别是 ```undefined null 0 NaN ''```除此之外都为真值

1 是真还是假，真 

0 是真还是假 假

'1' 是真还是假 真

'0' 是真还是假 真


## undefined 和 null 两种空类型
区别：
没有本质区别

细节一
如果一个变量声明了，但没有赋值，那么默认值就是 undefined，而不是 null

细节二
如果一个函数，没有写 return，那么默认 return undefined，而不是 null

细节三
前端程序员习惯上，把非对象的空值写为 undefined，把对象的空值写为 null
但仅仅是习惯上而已

## let声明
规则
* 遵循块作用域，即使用范围不能超出 { }

* 不能重复申明

* 可以赋值，也可以不赋值

* 必须先声明再使用，否则报错

* 全局声明的 let 变量，不会变成window 的属性

* for 循环配合 let 有奇效
## const 声明
规则
* 跟 let 几乎一样
* 只有一条不一样：声明时就要赋值，赋值后不能改
### name 和 'name' 的区别
* name 是变量
值可变，可能是 'name'，也可能是 'hello'
* 'name' 是字符串常量
常量就是不变量
'name' 只能是 'name'，不能是其他值
## 类型转换
* number => string
```
String(n)
n + ''
```
* string => number
```
Number(s)
parseInt(s) / parseFloat(s)
s - 0
```
* x => bool
```
Boolean(x)
!!x
```
* x => string
```
String(x)
x.toString()
```




