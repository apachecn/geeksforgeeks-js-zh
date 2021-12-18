# JavaScript | TypeDarray . ToLocalString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-type darray-tolocalesting-method/](https://www.geeksforgeeks.org/javascript-typedarray-tolocalestring-method/)

**TypeDarray . ToLocalString()**方法用于将元素转换为字符串，并由特定于区域设置的字符串分隔。

**语法:**

```
typedarray.toLocaleString( locales, options );
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Region:** This parameter holds the value of the region.
*   **option:** is an optional parameter.

**返回值:**这个方法返回一个代表 typedArray 元素的字符串。

下面的例子说明了 JavaScript 中的 typedArray.toLocaleString()方法:

**例 1:**

```
var geek = new Uint32Array([100, 897, 123, 132, 22]);

console.log(geek.toLocaleString()); 

console.log(geek.toLocaleString('en-US'));

console.log(geek.toLocaleString('hi', 
    { style: 'currency', currency: 'HIR' }));
```

**输出:**

```
"100, 897, 123, 132, 22"
"100, 897, 123, 132, 22"
"HIR 100.00, HIR 897.00, HIR 123.00, HIR 132.00, HIR 22.00"
```

**例 2:**

```
var A = " GeeksforGeeks ";  
var B = " JavaScript ";
var C = " Array.prototype.toLocaleString() ";
var D = [A, B, C];   
var result= D.toLocaleString();   
console.log(result);  
```

**输出:**

```
 " GeeksforGeeks, JavaScript, Array.prototype.toLocaleString() "
```

**支持的浏览器:**typedarray . tolocalestring()方法支持的浏览器如下: