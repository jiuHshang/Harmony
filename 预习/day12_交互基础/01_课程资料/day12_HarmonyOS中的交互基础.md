# day12_HarmonyOS中的交互基础

背景 : 在鸿蒙生态系统中 除了我们最基础的界面搭建 , 我们还需要使用交互效果让我们的网站动起来 ,  这样对于我们后面继续在鸿蒙开发学习有着很大的帮助 ; 

## 今日学习目标 

1. 什么是js
2. js作用
3. 如何使用js
4. js中变量的作用
5. 如何声明变量
6. js中常量的作用
7. 如何声明常量
8. js中的基础数据类型
9. js中的运算符
10. 数据类型转换

## 1. 什么是js

js是JavaScript的简称, 是一种弱文本类型的脚本编程语言, js是组成完整完成的一个组成部分; 一个网站组成分为: HTML结构 , CSS样式 ,JavaScript交互三个层次; 

## 2. js作用

JavaScript ( 后面统称js ) : 主要是用来做一系列的动态交互效果 , 让我们开发的网站实现动态的交互

## 3. JS使用位置

所有的js代码需要放在一个独立的以 .js 为后缀名的文件中, 并且需要通过script标签以及src属性来进行关联

```html
<script src="demo1.js"></script>
```

## 4. js中的注释

注释语句 : 使用的快捷键仍然是 ctrl + ?    显示样式为  :  //

## 5. js如何输出

### 1) 输出形式1

控制台输出 , 经常应用在代码测试位置 

```javascript
console.log("hello world")
```

### 2) 输出形式2

经常用于警告框

```javascript
alert("hello world")
```

### 3) 属性形式3

页面中输出

```JavaScript
//向页面中输出内容
document.write("hello world")
//向页面中输出一个并且能运行的标签
//注意:document向页面中输出的时候,如果输出内容为一个标签结构,则标签结构会被运行
document.write("<h1>我是一级标题</h1>")
```

## 6. 变量

变量 , 指的是一个可以变化的量 , 例如 : 身高, 体重等等

如何声明一个变量呢? 

变量定义的规则 : 

1. 不能以数字开头, 严禁使用汉字, 不能使用特殊符号
2. 可以使用字母, 数字, 下划线, $等

```JavaScript
//方式1 : 先声明后复制
var str1
str1=123
console.log(str1)
//方式2 : 声明并复制
var str2=234
console.log(str2)
```

## 7. 常量

常量 , 指的是一个不可以变化的量, 例如 : 圆周率 等

如何声明一个常量?

常量声明的时候, 为了避免出错, 我们都是直接声明并复制, 因为常量是不可以更改的 ; 所以我们复制直接声明

```javascript
const Pi = 3.14
```

## 8. 变量可实现的数据类型

### 1) 数值类型

包含一切数字和数值相关的内容 ( 特殊的数值类型NaN )

```JavaScript
var num1 = 100
```

### 2) 字符串类型

所有被引号包裹起来的内容

```javascript
var str1 = "abc"
```

### 3) 布尔类型

表示肯定或者是否定 , 主要应用于计算机表达式的应用场景

两种表达式形式 : 真或者是假

真使用 true 表示

假使用 false 表示

```javascript
var num1 = 3
var num2 = 4 
cosnole.log(num1>num2)
```

### 4) null空

null空类型, 代表变量有值, 值为空 , 只有再变量赋值的时候才能得到nul

```javascript
var str = null
```

### 5) undefined类型

undefined类型, 代表的是未定义, 代表的是没有值; 再声明变量, 没有赋值的时候经常出现

```javascript
var str
console.log(str)
```

### 6) 其他的复杂数据类型

后面我们会详细讲解

复杂数据类型里面有 : 函数 , 对象 , 数组 , 正则 等等

## 9. 如何检查数据类型

### 1) typeof()

typeof(变量) 来进行检查数据类型, 但是typeof只能检查基本数据类型, 复杂数据类型一律返回的值为Object



### 2) isNaN()

isNaN(变量) 来进行检查变量是不是一个数值 .  isNaN = is not a number

直译为 : 是的,不是一个数值

如果变量不是数值类型, 则返回布尔值 true

如果变量是数值类型, 则返回布尔值 false

```javascript
var str1 = "abc"
var str2 = 123
console.log(isNaN(str1)) //true
console.log(isNaN(str2)) //false
```



## 10. 案例 

1. 使用document方法向页面中输出 "一级标题---六级标题" 这样的标签 ( 提示每一行打印 )

2. 使用document方向向页面中输出一个一行一列的表格,  ( 提示每一行打印 )

3. 页面中窗口有一个输入弹窗, 来计算圆的面积, 再控制台输出 : "圆的面积为***"

   

## 11. 运算符

## 12. 数学运算符

### 1) +

加号运算符 , 只有左右都为数值类型才做加法运算, 只要有运算符一旁有一个字符串类型, 都完成的是字符串拼接的作用

```javascript
console.log("123"+"123")
console.log("123"+123)
console.log(123+123)
```

### 2) -

进行减法运算, 会自动把非数值类型转换成数值类型, 然后进行运算, 如果是不能转换, 则会按照NaN进行输出

```javascript
console.log("123" - 1)
console.log(123 - true)
console.log(123 - false)
console.log(123 - 'abc')
```

### 3) *

进行乘法运算, 会把运算符两侧都转换成数值进行运算

```javascript
console.log("123" * 1)
console.log(123 * true)
console.log(123 * false)
console.log(123 * 'abc')
```

### 4) /

进行除法运算, 会把运算符两侧都转换成数值进行运算

```javascript
console.log("123" / 1)
console.log(123 / true)
console.log(123 / false)
console.log(123 / 'abc')
```

### 5) %

进行取余运算 , 会把运算符两侧都转换成数值进行运算

```javascript
console.log("123" % 1)
console.log(123 % true)
console.log(123 % false)
console.log(123 % 'abc')
```



## 13. 赋值运算符

### 1) =

将运算符右侧的值赋值给左侧的变量, 使用左侧变量代替对应的值

```javascript
//将一些值赋值给对应的变量
var a = 124
var b = 'abc'
var c = true
console.log(a,b,c)
```

### 2) +=

在变量的基础上加上一个数值, 同时赋值给对应的变量

```javascript
var a =100
a = 100 + 5
console.log(a)
//简写
var b = 10
b+=5 // b = b + 5
console.log(b)
```

### 3) -=

在变量的基础上减去一个数值, 同时再赋值给对应的变量

```javascript
var a =100
a = 100 - 5
console.log(a)
//简写
var b = 10
b-=5 // b = b - 5
console.log(b)
```

### 4) *=

在变量的基础上乘以一个数值, 同时再赋值给对应的变量

```javascript
 var a =100
a = 100 * 5
console.log(a)
//简写
var b = 10
b*=5 // b = b * 5
console.log(b)
```

### 5) /=

在变量的基础上除以一个数值, 同时再赋值给对应的变量

```javascript
var a =100
a = 100 / 5
console.log(a)
//简写
var b = 10
b/=5 // b = b / 5
console.log(b)
```

### 6) %=

在变量的基础上取余一个数值, 同时再赋值给对应的变量

```javascript
var a =100
a = 100 % 3
console.log(a)
//简写
var b = 10
b%=5 // b = b % 5
console.log(b)
```



## 14. 比较运算符

用来比较大小 , 返回值为布尔类型

### 1) >

符号左侧大于右侧

```javascript
console.log(3>4)
console.log(4>3)
```

### 2) >=

符号左侧大于或者是等于右侧, 则返回真

```javascript
console.log(3>4)
console.log(4>3)
console.log(5>=5)
```

### 3) <

符号左侧小于右侧

```javascript
console.log(3<4)
console.log(4<3)
```

### 4) <=

符号左侧小于或者等于右侧,则返回真

```javascript
console.log(3<4)
console.log(4<3)
console.log(5<=5)
```

### 5) ==

符号左侧和右侧值相等即可, 就能返回真

```javascript
console.log("123"==123)
```

### 6) !=

比较符号两边的值是否不等,如果是返回true不管数据类型

```
console.log(1 != 1);
console.log(1 != "2")
```

## 15. 逻辑运算符

### 1) 与 (&&)

逻辑与 ,  并且的意思 , 符号左右同真则真 , 有假则假 

```javascript
console.log(true && false)
console.log(true && true)
```

### 2) 或 (||)

逻辑或 , 或者的意思 , 符号左右有真则真 , 同假才假

```javascript
console.log(true || false)
console.log(true || true)
console.log(false || false)
```

### 3) 非 (!)

取反

```javascript
console.log(!true)
console.log(!false)
```

## 16. 案例

1. 案例1 :使用字符串拼接的形式拼接一个一行一列的表格
2. 命名变量:姓名,身高,体重,年龄,性别并进行赋值
   	分别在 : 控制台,页面,弹窗中输出语句
   	语句格式 : "您的姓名是:**;您的性别是:**;您的年龄是:**;年的身高是:**;您的体重是:**"