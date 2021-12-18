# JavaScript symbol . matchell 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-matchell-property/](https://www.geeksforgeeks.org/javascript-symbol-matchall-property/)

下面是 Symbol.matchAll 属性的示例。

**示例:**

## Java Script 语言

```
<script>

// JavaScript to illustrate Symbol.matchAll property
function func() {

    // Regular expression
    const regExp = /[0-9]+/g;

    // Date
    const date = "06-03-2021";

    // finalResult store result of matchAll property
    const result = regExp[Symbol.matchAll](date);

    // Iterate on all matched elements
    console.log(Array.from(result, (x) => x[0]));
}

func();
</script>
```

*   **输出:**

```
["06", "03", "2021"]
```

Symbol.matchAll 属性返回与字符串匹配的正则表达式。string . prototype . matchell()方法调用此函数。属性的语法如下:

```
regExp[Symbol.matchAll](str);
```

**参数:**它使用一个字符串来查找正则表达式与该字符串的匹配。

**返回值:**symbol . matchell 属性返回一个迭代器，该迭代器返回与字符串匹配的正则表达式。

下面提供了上述功能的示例:

**例 1:**

```
const result = /a/[Symbol.matchAll]("abcd");
```

在本例中，Symbol.matchAll 属性返回一个迭代器，该迭代器返回与存储在结果中的字符串“abcd”匹配的正则表达式/a/a。因此，匹配的元素是["a"]。

**输出:**

```
["a"]
```

**例 2:**

```
const result = /[0-9]+/g[Symbol.matchAll]("06-03-2021");
```

在本例中，正则表达式的匹配元素是 06、03 和 2021。正则表达式[0-9]显示匹配的元素必须包含 0 到 9。g 表示进行全局搜索的全局。

**输出:**

```
["06","03","2021"]
```

**例 3:**

```
const result = /[0-9]+/g[Symbol.matchAll]
    ("India got freedom in 1947");
```

在本例中，正则表达式的匹配元素是 1947。因为唯一匹配的元素是 1947 年。

**输出:**

```
["1947"]
```

下面提供了上述功能的完整代码:

**程序 1:**

## Java Script 语言

```
<script>
    function func() {

        // Final Result store result of matchAll property
        const result = /a/[Symbol.matchAll]("abcd");

        // Iterate on all matched elements
        console.log(Array.from(result, (x) => x[0]));
    }

    func();
</script>
```

**输出:**

```
["a"]
```

**程序 2:**

## Java Script 语言

```
<script>
    function func() {

        // finalResult store result of matchAll property
        const result = /[0-9]+/g[Symbol.matchAll]("06-03-2021");

        // Iterate on all matched elements
        console.log(Array.from(result, (x) => x[0]));
    }

    func();
</script>
```

**输出:**

```
["06","03","2021"]
```

**程序 3:**

## Java Script 语言

```
<script>
    function func() {

        // finalResult store result of 
        // matchAll property
        const result = /[0-9]+/g[Symbol.matchAll]
            ("India got freedom in 1947");

        // Iterate on all matched elements
        console.log(Array.from(result, (x) => x[0]));
    }

    func();
</script>
```

**输出:**

```
["1947"]
```