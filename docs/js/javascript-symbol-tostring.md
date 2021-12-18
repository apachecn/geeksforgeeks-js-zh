# JavaScript | symbol . ToString()

> 原文:[https://www.geeksforgeeks.org/javascript-symbol-tostring/](https://www.geeksforgeeks.org/javascript-symbol-tostring/)

**符号. toString()** 是 JavaScript 中的一个内置函数，用于*将指定的符号对象转换为字符串*。

**语法:**

```
Symbol().toString();
```

这里**符号()**是指定的要转换成字符串的符号对象。

**参数:**此功能不接受任何参数。

**返回值:**该函数返回指定符号对象的转换字符串。

JavaScript 代码展示了这个函数的工作原理:
**示例-1:**

```
<script>

    // Creating some Symbol objects
    const A = Symbol('gfg');
    const B = Symbol(42);
    const C = Symbol();

    // Calling toString() function
    a = A.toString();
    b = B.toString();
    c = C.toString();

    // Printing the strings which represent
    // the above specified Symbol object
    document.write(a + "<br>");
    document.write(b + "<br>");
    document.write(c);

</script>
```

**输出:**

```
Symbol(gfg)
Symbol(42)
Symbol()
```

**示例-2:**

```
<script>

   // Creating some Symbol object and
   // Calling toString() function
   a = Symbol('Geeks').toString();
   b = Symbol.iterator.toString();
   c = Symbol.for('Geeks').toString();

   // Printing the strings which represent
   // the above specified Symbol object
   document.write(a +"<br>");
   document.write(b +"<br>");
   document.write(c);

</script>
```

**输出:**

```
Symbol(Geeks)
Symbol(Symbol.iterator)
Symbol(Geeks)
```

**支持的浏览器:**

*   苹果 Safari 9
*   边缘 12
*   Firefox 36
*   谷歌 Chrome 38
*   歌剧 25

**参考:**[https://devdocs . io/JavaScript/global _ objects/symbol/tostring](https://devdocs.io/javascript/global_objects/symbol/tostring)