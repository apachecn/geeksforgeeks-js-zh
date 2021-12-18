# JavaScript | Intl。datetime format . prototype . formattoprts()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-datetime format-prototype-formattoparts-method/](https://www.geeksforgeeks.org/javascript-intl-datetimeformat-prototype-formattoparts-method/)

**国际号码。DateTimeFormat . prototype . formattoprts()**方法是 JavaScript 中的一个内置方法，它允许对 datetime format 格式化程序生成的字符串进行区域设置感知格式化。
**语法:**

```
dateTimeFormat.formatToParts( date )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **日期:**为可选参数，保存要格式化的日期。

**返回值:**这个方法返回一个包含格式化日期的数组。
下面的例子说明了**国际号码。【JavaScript 中的 T4】:
**示例 1:**** 

## java 描述语言

```
let geeks = {month: 'numeric', day: 'numeric', year: "numeric"};
let result =  new Intl.DateTimeFormat("en-u-ca-chinese", geeks);
let datetime = Date.UTC(2012, 11, 17, 3);
let val = result.formatToParts(datetime);
console.log(val[0]);
console.log(val[1]);
console.log(val[2]);
console.log(val[3]);
```