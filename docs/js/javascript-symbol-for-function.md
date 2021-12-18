# JavaScript | Symbol.for()函数

> 原文:[https://www . geesforgeks . org/JavaScript-符号换函数/](https://www.geeksforgeeks.org/javascript-symbol-for-function/)

**Symbol.for()** 是 JavaScript 中的一个内置函数，用于在运行时范围内的符号注册表中搜索给定的符号，如果找到，则返回相同的符号，否则它会在全局符号注册表中创建一个与给定符号同名的新符号并返回它们。

**语法:**

```
Symbol.for(key);

```

这里**“符号”**是要搜索到运行时范围的符号注册表中的符号。

**参数:**该函数接受一个参数“key”，它是符号的键，用于符号的描述。

**返回值:**此函数返回在运行时范围的符号注册表中找到的给定符号，否则创建一个与给定符号同名的新符号并返回。

**JavaScript 代码展示此功能的工作方式:**
**示例-1:**

```
<script >
    // Some symbols are created
    const symbol1 = Symbol.for('Geeks');
    const symbol2 = Symbol.for(123);
    const symbol3 = Symbol.for("gfg");
    const symbol4 = Symbol.for('789');

    // Getting the same symbols if found 
    // in the global symbol registry
    // otherwise a new created and returned
    console.log(symbol1);
    console.log(symbol2);
    console.log(symbol3);
    console.log(symbol4);
</script>
```

**输出:**

```
> Symbol(Geeks)
> Symbol(123)
> Symbol(gfg)
> Symbol(789)

```

**示例-2:**

```
<script>
    // Some symbols are created
    const symbol1 = Symbol.for('a', 'b', 'c');
    const symbol2 = Symbol.for(1, 2, 3);
    const symbol3 = Symbol.for(1 + 2);
    const symbol4 = Symbol.for("Geeks" + "for" + "Geeks");

    // Getting the same symbols if found 
    // in the global symbol registry
    // otherwise a new created and returned
    console.log(symbol1);
    console.log(symbol2);
    console.log(symbol3);
    console.log(symbol4); 
</script>
```

**输出:**

```
> Symbol(a)
> Symbol(1)
> Symbol(3)
> Symbol(GeeksforGeeks)

```

在上面的代码中，键不应该是多重的，否则它会接受第一个元素作为键，并丢弃剩余的元素，如果使用某个算术运算符来代替键，则该函数会将该键视为操作的结果。

**支持的浏览器:**

*   谷歌 Chrome 40 及以上
*   边缘 12 及以上
*   Firefox 36 及以上版本
*   歌剧 27 及以上
*   Safari 9 及以上

**参考:**T2】https://devdocs.io/javascript/global_objects/symbol/for