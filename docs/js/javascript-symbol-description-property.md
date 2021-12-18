# JavaScript | symbol . description 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-description-property/](https://www.geeksforgeeks.org/javascript-symbol-description-property/)

**符号描述**是 JavaScript 中的一个内置属性，用于*返回指定符号对象*的可选描述。

**语法:**

```
A.description;
```

这里**“A”**是指定的符号对象，可以是**符号(【任意值】)**、**符号迭代器**、**符号 for(【任意值】)**等。

**参数:**该属性不接受任何参数。

**返回值:**该属性返回指定符号对象的可选描述。

JavaScript 代码展示了这个函数的工作原理:
**示例-1:**

```
<script>

   // Calling description property over
   // some specified symbol objects
   document.write(Symbol('Geek').description +"<br>");
   document.write(Symbol.iterator.description +"<br>");
   document.write(Symbol.for('GeeksforGeeks').description +"<br>");
   document.write(Symbol('Geeks').description + 'forGeeks');

</script>
```

**输出:**

```
Geek
Symbol.iterator
GeeksforGeeks
GeeksforGeeks

```

**示例-2:**

```
<script>

   // Calling description property over
   // a specified symbol objects
   document.write(Symbol().description +"<br>");

</script>
```

**输出:**

```
undefined
```

在上面的代码中，符号对象“symbol()”应该有一些参数，否则它会给出未定义的输出。

**支持的浏览器:**

*   Chrome 70 及以上
*   边缘 79 及以上
*   Firefox 63 及以上版本
*   歌剧 57 及以上
*   Safari 12.1 及以上版本

**参考:**[https://devdocs . io/JavaScript/global _ objects/symbol/description](https://devdocs.io/javascript/global_objects/symbol/description)