# JavaScript | object . isextensable()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-isextensible-method/](https://www.geeksforgeeks.org/javascript-object-isextensible-method/)

JavaScript 中的**object . PrevenTextExtensions()方法**是标准的内置对象，用于检查对象是否可扩展。
**语法:**

```
Object.isExtensible( obj )
```

**参数:**该方法接受上述单个参数，描述如下:

*   **obj:** 此参数保存应检查可延展性的对象。

**返回值:**该方法返回一个布尔值，指示给定对象是否可扩展。
以下示例说明了 JavaScript 中的 Object.isExtensible()方法:
**示例 1:**

## java 描述语言

```
const geeks1 = {};
console.log(Object.isExtensible(geeks1));
Object.preventExtensions(geeks1);
console.log(Object.isExtensible(geeks1));

const geeks2 = {}; 
Object.preventExtensions(geeks2); 
console.log( 
    Object.isExtensible(geeks2) 
); 
```

**输出:**

```
true
false
false
```

**例 2:**

## java 描述语言

```
var geeks1 = {};
document.writeln(Object.isExtensible(geeks1));
document.writeln("<br>");
document.writeln(Object.preventExtensions(geeks1));
document.writeln("<br>");
document.writeln(Object.isExtensible(geeks1));
document.writeln("<br>");

var geeks2 = Object.seal({});
document.writeln(Object.isExtensible(geeks2));
document.writeln("<br>");

var geeks3 = Object.freeze({});
document.writeln(Object.isExtensible(geeks3));
```

**输出:**

```
true
[object Object]
false
false
false
```

**支持的浏览器:**object . isextensible()方法支持的浏览器如下:

*   谷歌 Chrome 6 及以上版本
*   边缘 12 及以上
*   Firefox 4 及以上版本
*   Internet Explorer 9
*   歌剧 12 及以上
*   Safari 5.1 及以上版本