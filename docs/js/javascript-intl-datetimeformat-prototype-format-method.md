# JavaScript | Intl。datetime format . prototype . format()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-datetime format-prototype-format-method/](https://www.geeksforgeeks.org/javascript-intl-datetimeformat-prototype-format-method/)

**国际号码。datetime format . prototype . format()**方法是 JavaScript 中的一个内置方法，用于根据此 Intl 的区域设置和格式选项来格式化日期。DateTimeFormat 对象。
**语法:**

```
dateTimeFormat.format( date )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **日期:**此参数保存需要格式化的日期。

下面的例子说明了 **Intl。datetime format . prototype . format()方法【JavaScript 中的 T1:
**示例 1:**** 

## java 描述语言

```
const Geeks = { weekday: 'long', year:
'numeric', month: 'long', day: 'numeric' };
const dateformat = new Date(1997, 06, 30);

const dateTimeFormat4 = new Intl.DateTimeFormat('hi', Geeks);
console.log(dateTimeFormat4.format(dateformat));

const dateTimeFormat2 = new Intl.DateTimeFormat('en-GB', Geeks);
console.log(dateTimeFormat2.format(dateformat));

const dateTimeFormat1 = new Intl.DateTimeFormat('sr-RS', Geeks);
console.log(dateTimeFormat1.format(dateformat));

const dateTimeFormat3 = new Intl.DateTimeFormat('en-US', Geeks);
console.log(dateTimeFormat3.format(dateformat));
```