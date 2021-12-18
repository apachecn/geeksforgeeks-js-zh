# 矩量法

> 原文:[https://www . geesforgeks . org/moment-js-moment-second-method/](https://www.geeksforgeeks.org/moment-js-moment-second-method/)

**时刻()。second()** 方法用于从当前时间获取秒数或设置秒数。

**语法:**

```
moment().second();
```

//或者

```
moment().seconds();
```

**参数:**此方法接受您想要设置秒的单个参数编号，然后您将需要一个附加参数:

*   **Number:** Its range is from 0 to 59, which is used to set the second in the variable.

**返回值:**该函数以秒为单位返回当前时间。

**注意:**这在正常的 Node.js 程序中无法工作，因为它需要安装 moment.js 库。

可以使用以下命令安装 moment . js:

```
npm install moment
```

**示例 1:** 获取当前时间(秒)。

## Javascript

```
// Acquiring the plugin 
const moment = require('moment'); 

var sec = moment().second(); 

console.log("Current seconds Time:", sec);
```

**输出:**

```
Current seconds Time: 18
```

**例 2:** 设置秒时间。

## Javascript

```
// Acquiring the plugin 
const moment = require('moment'); 

var sec = moment().second(55); 

console.log("Seconds Time:", sec);
```

**输出:**我们可以看到时间的秒数。

```
Seconds Time: Moment<2020-08-05T20:59:55+05:30>
```