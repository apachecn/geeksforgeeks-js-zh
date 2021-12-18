# JavaScript | string . prototype . tolocalelowercase()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-tolocalelowercase-method/](https://www.geeksforgeeks.org/javascript-string-prototype-tolocalelowercase-method/)

JavaScript 中的**string . prototype . tolocalelowercase()方法**是一个标准的内置对象，它返回基于主机当前区域设置转换为小写字母的调用字符串值。

**语法:**

```
str.toLocaleLowerCase()
str.toLocaleLowerCase(locale) 
str.toLocaleLowerCase([locale, locale, ...])
```

**参数:**

*   **区域设置:**是可选参数，表示根据任何特定于区域设置的大小写映射转换为小写的区域设置。

**返回值:**这个方法返回一串小写字母。

**异常:**该方法给出两种误差，如下:

*   ***范围错误* :** 如果区域设置参数不是有效的语言标签。
*   ***类型错误* :** 如果数组元素不是字符串类型。

下面的例子说明了 JavaScript 中的 string . prototype . tolocalelowercase()方法:

**例 1:**

```
const gfg = 'GeeKsForGeekS';
console.log('EN-US: ' + gfg.toLocaleLowerCase('en-US'));
console.log('TR: ' + gfg.toLocaleLowerCase('tr'));

const gfg1 = new String("String.prototype.toLocaleLowerCase()");
console.log('Result: ' + gfg1.toLocaleLowerCase());
```

**输出:**

```
"EN-US: geeksforgeeks"
"TR: geeksforgeeks"
"Result: string.prototype.tolocalelowercase()"
```

**例 2:**

```
console.log('ALPHABET'.toLocaleLowerCase());

console.log('\u0130'.toLocaleLowerCase('tr') === 'i');  
console.log('\u0130'.toLocaleLowerCase('en-US') === 'i');

let geeks = ['tr', 'TR', 'tr-TR', 'tr-u-co-search', 'tr-x-turkish'];
console.log('\u0130'.toLocaleLowerCase(geeks) === 'i'); 
```

**输出:**

```
"alphabet"
true
false
true
```

**支持的浏览器:**string . prototype . tolocalowercase()方法支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   工业管理学(Industrial Engineering)
*   歌剧
*   旅行队
*   边缘