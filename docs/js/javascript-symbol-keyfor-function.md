# JavaScript | Symbol.keyFor()函数

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-key for-function/](https://www.geeksforgeeks.org/javascript-symbol-keyfor-function/)

**Symbol.keyFor()** 是 JavaScript 中的一个内置函数，用于*检索与给定符号*共享的密钥，该密钥从全局符号注册表中检索。

**语法:**

```
Symbol.keyFor(sym);

```

这里**“符号”**是要搜索到运行时范围的符号注册表中的符号。

**参数:**该函数接受一个参数**“符号”**，该参数是要找到密钥的符号。

**返回值:**该函数返回一个字符串，代表在全局注册表中找到的给定符号的键，否则返回 undefined。

显示该函数工作情况的 JavaScript 代码。
**例-1:**

```
<script>
    // Some symbols are created
    // with proper key
    const sym1 = Symbol.for('Geeks');
    const sym2 = Symbol.for(123);
    const sym3 = Symbol.for("gfg");
    const sym4 = Symbol.for('789');

    // Calling the keyFor() function and
    // getting the key for the above symbols
    console.log(Symbol.keyFor(sym1));
    console.log(Symbol.keyFor(sym2));
    console.log(Symbol.keyFor(sym3));
    console.log(Symbol.keyFor(sym4)); 
</script>
```

**输出:**

```
"Geeks"
"123"
"gfg"
"789"

```

**示例-2:**

```
<script>
    // Creating some symbols without key
    const sym1 = Symbol.for();
    const sym2 = Symbol.iterator;

    // Calling the keyFor() function and
    // getting the key for the above symbols
    console.log(Symbol.keyFor(sym1));
    console.log(Symbol.keyFor(sym2)); 
</script>
```

**输出:**

```
"undefined"
"undefined"

```

**支持的浏览器:**

*   谷歌 Chrome 40 及以上
*   边缘 12 及以上
*   Firefox 36 及以上版本
*   歌剧 27 及以上
*   Safari 9 及以上

**参考:**T2】https://devdocs.io/javascript/global_objects/symbol/keyfor