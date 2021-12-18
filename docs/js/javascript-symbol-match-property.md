# JavaScript | Symbol.match 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-match-property/](https://www.geeksforgeeks.org/javascript-symbol-match-property/)

JavaScript 中的 **Symbol.match** 属性是一个众所周知的符号，用于识别正则表达式与字符串的匹配，这个函数使用 **String.prototype.match()方法**调用。

**语法:**

```
regexp[Symbol.match] = false;
```

**参数:**不接受任何参数。

**返回值:**返回匹配字符串的布尔值，如果匹配，则返回真，否则返回假。

以下示例说明了 JavaScript 中的 Symbol.match 属性:

**例 1:**

```

const regexp1 = /geeksforgeeks/;

regexp1[Symbol.match] = false;

document.write('/geeks/'.startsWith(regexp1));
document.write('/geeksforgeeks/'.endsWith(regexp1));
```

**输出:**

```
false
true

```

**示例 2:** 本示例返回类型错误。

```

reg[Symbol.match] = false;  

console.log('/bar/'.startsWith(/bar/));  
```

**输出:**

```
Error: First argument to String.prototype.startsWith must not be a regular expression.

```

**支持的浏览器:**symbol . match 属性支持的浏览器如下:

*   谷歌铬合金 51
*   Firefox 50
*   边缘 15
*   歌剧
*   苹果旅行队

**参考:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Global _ Objects/Symbol/match](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/match)