# 矩. js 矩.分()法

> 原文:[https://www . geesforgeks . org/moment-js-moment-minute-method/](https://www.geeksforgeeks.org/moment-js-moment-minute-method/)

**时刻()。minute()** 方法用于从当前时间获取分钟或设置分钟。

**语法** :

```
moment().minute();
```

或者

```
moment().minutes();
```

**参数**:这个方法接受一个你想设置分钟数的参数，然后你需要一个额外的参数:

**数字:**范围从 0 到 59，用于在变量中设置分钟。

**返回值:**该函数以分钟为单位返回当前时间。

**注意:**这在正常的 Node.js 程序中不会起作用，因为它需要一个外部的 moment.js 库全局安装或者安装在项目目录中。

可以使用以下命令安装 Moment.js:

**安装模块:**

```
npm install moment
```

**示例 1:** 获取当前时间(分钟)。

## 

```
// Importing moment module
const moment = require('moment'); 

var a = moment().minutes();

console.log("minute is: ",a); 
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
minute is:  24
```

**示例 2:** 设置分钟时间。

## 

```
// Importing moment module
const moment = require('moment'); 

var a = moment().minutes(20);
// Printing the updated minutes
console.log(a); 
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Moment<2021-02-10T22:20:29+05:30>
```

**参考:**T2】https://momentjs.com/docs/#/get-set/minute/