js的三座大山：原型和原型链 this AJAX


伪数组：没有数组的共有属性例如：push等 


不给任何条件，this默认指向window

如何传this和arguments？

用fn.call(xxx,1,2,3) xxx为this 123为arguments

xxx会自动转换成对象（js的糟粕）

例如：
```
function fn(){
    'use strict'//如果不加这句则js会默认会将传的东西变成对象
    console.log(this)
}