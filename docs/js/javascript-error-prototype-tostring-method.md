# JavaScript | error . prototype . tostring()方法

> 原文:[https://www . geesforgeks . org/JavaScript-error-prototype-tostring-method/](https://www.geeksforgeeks.org/javascript-error-prototype-tostring-method/)

**Error . prototype . ToString()**方法是 JavaScript 中的一个内置方法，用于返回表示指定 Error 对象的字符串。

**语法:**

```
e.toString()
```

**参数:**此方法不接受任何参数。

**返回值:**这个方法返回一个代表指定错误对象的字符串。

下面的例子说明了 JavaScript 中的 Error.prototype.toString()方法:

**例 1:**

```
var geeks1 = new Error();
document.writeln(geeks1.toString()); 
document.writeln("<br>");

geeks1.name = undefined;
document.writeln(geeks1.toString()); 
document.writeln("<br>");

geeks1.name = 'GeeksForGeeks';
document.writeln(geeks1.toString());
```

**输出:**

```
Error
Error
GeeksForGeeks

```

**例 2:**

```
var geeks = new Error('Error.prototype.toString()');
document.writeln(geeks.toString()); 
document.writeln("<br>");

geeks.name = undefined;
document.writeln(geeks.toString()); 
document.writeln("<br>");

geeks.name = '';
document.writeln(geeks.toString()); 
document.writeln("<br>");

geeks.message = "Error Type";
document.writeln(geeks.toString());
document.writeln("<br>");

geeks.message = undefined;
document.writeln(geeks.toString());
document.writeln("<br>");

geeks.name = 'GeeksForGeeks';
document.writeln(geeks.toString());
```

**输出:**

```
Error: Error.prototype.toString()
Error: Error.prototype.toString()
Error.prototype.toString()
Error Type

GeeksForGeeks
```

**支持的浏览器:**error . prototype . tostring()方法支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   边缘