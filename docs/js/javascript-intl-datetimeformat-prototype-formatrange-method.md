# JavaScript | Intl。datetime format . prototype . format range()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-datetime format-prototype-format range-method/](https://www.geeksforgeeks.org/javascript-intl-datetimeformat-prototype-formatrange-method/)

**国际号码。datetime format . prototype . format range()**方法是 JavaScript 中的内置方法，用于根据实例化 Intl 时提供的区域设置和选项，以最简洁的方式格式化日期范围。DateTimeFormat 对象。
**语法:**

```
Intl.DateTimeFormat.prototype.formatRange(startDate, endDate)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **开始日期:**此参数保存范围的开始日期。
*   **结束日期:**此参数保存范围的结束日期。

下面的例子说明了 **Intl。datetime format . prototype . format range()方法【JavaScript 中的 T1:
**示例 1:**** 

## java 描述语言

```
const geeks1 = { weekday: 'long', year: 'numeric',
                 month: 'long', day: 'numeric' };
const geeks2 = { year: '2-digit', month: 'numeric',
                 day: 'numeric' };

const startDate = new Date(Date.UTC(1997, 5, 30, 3, 3, 3));
const endDate = new Date(Date.UTC(2073, 7, 6, 11, 0, 0));

const dateTime = new Intl.DateTimeFormat('en', geeks1);
console.log(dateTime.formatRange(startDate, endDate));

const dateTime1 = new Intl.DateTimeFormat('hi', geeks1);
console.log(dateTime1.formatRange(startDate, endDate));

const dateTime2 = new Intl.DateTimeFormat('en', geeks2);
console.log(dateTime2.formatRange(startDate, endDate));

const dateTime3 = new Intl.DateTimeFormat('hi', geeks2);
console.log(dateTime3.formatRange(startDate, endDate));
```