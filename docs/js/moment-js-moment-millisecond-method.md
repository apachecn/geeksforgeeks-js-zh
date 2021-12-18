# Moment.js moment()。毫秒()方法

> 原文:[https://www . geesforgeks . org/moment-js-moment-毫秒-method/](https://www.geeksforgeeks.org/moment-js-moment-millisecond-method/)

**时刻()。毫秒()** 方法用于从时间中获取毫秒或设置毫秒。

**语法:**

```
moment().millisecond();
```

//或者

```
moment().milliseconds();
```

**参数:**该方法接受用于设置毫秒的单个参数号，然后您将需要一个附加参数:

*   **No.:** It ranges from 0 to 1000 and is used to set milliseconds in variables.

**返回值:**该函数以毫秒为单位返回当前时间。

**注意:**这在正常的 Node.js 程序中无法工作，因为它需要安装 moment.js 库。

可以使用以下命令安装 moment . js:

```
npm install moment
```

**示例 1:** 获取当前时间，单位为毫秒。

## Javascript

```
// Acquiring the plugin 
const moment = require('moment'); 

var mili = moment().millisecond(); 

console.log("Current Milliseconds Time:", mili);
```

**输出:**

```
Current Milliseconds Time: 274
```

**示例 2:** 在变量中设置毫秒时间。

## Javascript

```
// Acquiring the plugin 
const moment = require('moment'); 

var mili = moment(199).millisecond(); 

console.log("Milliseconds Time:", mili);
```

**输出:**

```
Milliseconds Time: 199
```