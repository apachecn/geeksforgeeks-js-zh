# JavaScript |符号。@@toPrimitive()功能

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-to primitive-function/](https://www.geeksforgeeks.org/javascript-symbol-toprimitive-function/)

**符号。@ @ topprimitive()**是 JavaScript 中的一个内置函数，用于*将给定的符号对象转换为一个基元值*。

**语法:**

```
Symbol()[Symbol.toPrimitive](hint);

```

这里 **Symbol()** 是要找到原值的符号对象。

**参数:**该功能接受可选参数**【提示】**。

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

    // Calling the symbol.@@toPrimitive() function
    var result1 = symbol1[Symbol.toPrimitive]("Value");
    var result2 = symbol2[Symbol.toPrimitive]("String");
    var result3 = symbol3[Symbol.toPrimitive](789);
    var result4 = symbol4[Symbol.toPrimitive]();

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

在上面的代码中，可以看到可选参数“提示”可以是值、字符串、任意整数值等。

**示例-2:**

```
<script>
    // a symbol object is created
    const symbol = Symbol('gfg');

    // Calling the symbol.@@toPrimitive() function
    var result = symbol[Symbol.toPrimitive];

    // Getting the primitive value 
    console.log(result);
</script>
```

**输出:**

```
> function [Symbol.toPrimitive]() { [native code] }

```

在上面的代码中，可以看到括号应该用于“提示”参数，否则它会给出类似上面输出的结果。

**支持的浏览器:**

*   谷歌 Chrome 47 及以上
*   Firefox 44
*   边缘 15 及以上
*   歌剧 34 及以上
*   Apple Safari 10 及以上版本

**参考:**[https://devdocs . io/JavaScript/global _ objects/symbol/@ @ topprimitive](https://devdocs.io/javascript/global_objects/symbol/@@toprimitive)