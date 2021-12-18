# JavaScript | symbol.valueOf()函数

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-value of-function/](https://www.geeksforgeeks.org/javascript-symbol-valueof-function/)

**符号.值 Of()** 是 JavaScript 中的一个内置函数，用于*返回给定符号对象的原始值。*

**语法:**

```
Symbol().valueOf();

```

这里 **Symbol()** 是要找到原值的符号对象。

**参数:**该函数不取任何参数。

**返回值:**该函数返回给定符号对象的基元值。

显示该函数工作情况的 JavaScript 代码。
**例-1:**

```
<script>
    // Some symbol objects are created
    const symbol1 = Symbol('Geeks');
    const symbol2 = Symbol("Geeks");
    const symbol3 = Symbol(123);
    const symbol4 = Symbol();

    // Calling the symbol.valueOf() function
    var result1 = symbol1.valueOf();
    var result2 = symbol2.valueOf();
    var result3 = symbol3.valueOf();
    var result4 = symbol4.valueOf();

    // Getting the primitive value 
    console.log(result1);
    console.log(result2);
    console.log(result3);
    console.log(result4);
</script>
```

**输出:**

```
> Symbol(Geeks)
> Symbol(Geeks)
> Symbol(123)
> Symbol()

```

**示例-2:**

```
<script>
    // Some symbol objects are created
    const symbol1 = Symbol('Geeks' + 'for' + 'Geeks');
    const symbol2 = Symbol(2+3);
    const symbol3 = Symbol(10/5);
    const symbol4 = Symbol(1, 2, 3);

    // Calling the symbol.valueOf() function
    var result1 = symbol1.valueOf();
    var result2 = symbol2.valueOf();
    var result3 = symbol3.valueOf();
    var result4 = symbol4.valueOf();

    // Getting the primitive value 
    console.log(result1);
    console.log(result2);
    console.log(result3);
    console.log(result4);
</script>
```

**输出:**

```
> Symbol(GeeksforGeeks)
> Symbol(5)
> Symbol(2)
> Symbol(1)

```

在上面的代码中，可以看到符号对象的参数应该是单个参数，否则它会将第一个元素视为参数，其余的将被丢弃。如果参数是一个算术运算，那么它会将它们视为作为参数的运算结果。

**支持的浏览器:**

*   Chrome 38 及以上
*   边缘 12 及以上
*   Firefox 36 及以上版本
*   歌剧 25 及以上
*   Safari 9 及以上

**参考:**T2】https://devdocs.io/javascript/global_objects/symbol/valueof