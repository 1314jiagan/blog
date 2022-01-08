
# 如下代码，为何会打印出6个6？
```
let i = 0
for(i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```
setTimeout(?,0)，表示立即执行，但是也是有一段时间的，在i=6时，开始打印出结果，结果就是6个6；相当于以下的代码
```
for(var i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```
但是将以上的var 改成 let ，就会输出0，1，2，3，4，5。
```
for (var i=0; i<6; i++) {

!(function (i){setTimeout(() => console.log(i),0)})(i)

}
```
利用立即执行函数将i打印出也是0，1，2，3，4，5。

