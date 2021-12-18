# JavaScript | Intl。datetime format . prototype . resolved options()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-datetime format-prototype-resolved options-method/](https://www.geeksforgeeks.org/javascript-intl-datetimeformat-prototype-resolvedoptions-method/)

**国际号码。DateTimeFormat . prototype . resolved options()**方法是 JavaScript 中的一个内置方法，它返回一个新对象，该对象的属性反映了在初始化此 datetime format 对象期间计算的区域设置、日期和时间格式选项。
**语法:**

```
dateTimeFormat.resolvedOptions()
```

**参数:**此方法不接受任何参数。
**返回值:**该方法返回一个新对象，该对象的属性反映了区域设置以及日期和时间。
以下示例说明了 **Intl。datetime format . prototype . resolved options()方法【JavaScript 中的 T7】:
**示例 1:**** 

## java 描述语言

```
const geeks = new Intl.DateTimeFormat('zh-CN', { timeZone: 'UTC' });
const result = geeks.resolvedOptions();
console.log(result.locale);
console.log(result.calendar);
console.log(result.timeZone);

const geeks1 = new Intl.DateTimeFormat('LT');
const result1 = geeks1.resolvedOptions();
console.log(result1.locale);
console.log(result1.calendar);
```

**输出:**

```
"zh-CN"
"gregory"
"UTC"
"lt"
"gregory"
```

**例 2:**

## java 描述语言

```
var geeks = new Intl.DateTimeFormat('de-XX', { timeZone: 'UTC' });
var result = geeks.resolvedOptions();

console.log(result.locale);      
console.log(result.calendar);      
console.log(result.numberingSystem);
console.log(result.timeZone);       
console.log(result.month);
```

**输出:**

```
"de"
"gregory"
"latn"
"UTC"
"numeric"
```

**支持的浏览器:**T2 国际机场支持的浏览器。方法如下所示:

*   谷歌 Chrome 24 及以上版本
*   边缘 12 及以上
*   Firefox 29 及以上版本
*   歌剧 15 及以上
*   Safari 10 及以上