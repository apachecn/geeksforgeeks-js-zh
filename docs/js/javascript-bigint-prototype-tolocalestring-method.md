# JavaScript | Bigint . prototype . ToLocalString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-bigint-prototype-tolocalesting-method/](https://www.geeksforgeeks.org/javascript-bigint-prototype-tolocalestring-method/)

**BigInt . prototype . ToLocalString()**方法是 JavaScript 中的一个内置方法，用于返回一个字符串，该字符串具有该 Bigint 的语言敏感表示。
**语法:**

```
bigIntObj.toLocaleString(locales, options)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **地区:**此参数保存地区的值。
*   **选项:**为可选参数。

**返回值:**该方法返回一个字符串，该字符串具有给定 BigInt 的语言敏感表示。
下面的例子说明了 JavaScript 中的 bigint . prototype . tolocalesting()方法:
**例子 1:**

## java 描述语言

```
let geekvar = 45334n;
console.log(geekvar.toLocaleString());

geekvar =78753456789123456789n;
console.log(geekvar.toLocaleString('de-DE'));
console.log(geekvar.toLocaleString('de-DE',
    { style: 'currency', currency: 'EUR' }));
console.log(geekvar.toLocaleString('hi'));
```