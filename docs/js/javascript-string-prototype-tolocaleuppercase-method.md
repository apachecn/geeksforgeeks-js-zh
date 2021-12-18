# JavaScript | string . prototype . tolocaleuppercese()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-tolocaleuppercese-method/](https://www.geeksforgeeks.org/javascript-string-prototype-tolocaleuppercase-method/)

JavaScript 中的**string . prototype . tolocaleuppercese()方法**是一个标准的内置对象，它返回基于主机当前区域设置转换为大写字母的调用字符串值。

**语法:**

```
str.toLocaleUpperCase()
str.toLocaleUpperCase(locale) 
str.toLocaleUpperCase([locale, locale, ...])
```

**参数:**

*   **区域设置:**这是一个可选参数，该区域设置参数表示根据任何特定于区域设置的大小写映射转换为大写的区域设置。

**返回值:**这个方法返回一个大写字母的字符串。

**异常:**该方法给出两种误差，如下:

*   ***范围错误* :** 如果区域设置参数不是有效的语言标签。
*   ***类型错误* :** 如果数组元素不是字符串类型。

下面的例子说明了 JavaScript 中的 string . prototype . tolocaleuppercese()方法:

**例 1:**

```
const gfg = 'GeeKsForGeekS';
console.log('EN-US: ' + gfg.toLocaleUpperCase('en-US'));
console.log('TR: ' + gfg.toLocaleUpperCase('tr'));

const gfg1 = new String("String.prototype.toLocaleUpperCase()");
console.log('Result: ' + gfg1.toLocaleUpperCase());
```

**输出:**

```
"EN-US: GEEKSFORGEEKS"
"TR: GEEKSFORGEEKS"
"Result: STRING.PROTOTYPE.TOLOCALEUPPERCASE()"
```

**例 2:**

```
console.log('ALPHABET'.toLocaleUpperCase());

console.log('i\u0307'.toLocaleUpperCase('tr') === 'I');  
console.log('i\u0307'.toLocaleUpperCase('lt-LT') === 'I');

let geeks = ['lt', 'LT', 'lt-LT', 'lt-u-co-phonebk', 'lt-x-lietuva'];
console.log('i\u0307'.toLocaleUpperCase(geeks) === 'I'); 
```

**输出:**

```
"ALPHABET"
false
true
true
```

**支持的浏览器:**string . prototype . tolocaleuppercese()方法支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   工业管理学(Industrial Engineering)
*   歌剧
*   旅行队
*   边缘