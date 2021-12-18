# 矩. js 矩.小时()法

> 原文:[https://www.geeksforgeeks.org/moment-js-moment-hour-method/](https://www.geeksforgeeks.org/moment-js-moment-hour-method/)

**时刻()。hour()** 方法用于从当前时间获取小时数或设置小时数。

**语法** :

```
moment().hour();
```

或者

```
moment().hours();
```

**参数**:这个方法接受一个你想要设置小时数的单个参数，然后你需要一个额外的参数:

**数字:**:范围从 0 到 23，用于在变量中设置小时。

**返回值:**该函数以小时为单位返回当前时间

**注意:**这在正常的 Node.js 程序中是行不通的，因为它需要一个外部的 moment.js 库全局安装或者安装在项目目录中。

可以使用以下命令安装 Moment.js:

**安装模块:**

```
npm install moment
```

**例 1:** 获取当前时间，单位为小时。

## 

```
// Importing moment module 
const moment = require('moment'); 

var a = moment().hours();

console.log("hours is: ",a); 
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
hours is:  22
```

**例 2** :设置时间小时。

**索引. js**

## 【JavaScript】

```
// Importing moment module
const moment = require('moment'); 

var a = moment().hours(20);

console.log(a); 
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Moment<2021-02-10T20:34:30+05:30>
```

**参考:**T2】https://momentjs.com/docs/#/get-set/hour/