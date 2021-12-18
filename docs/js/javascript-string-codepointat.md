# JavaScript string . code point()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-string-code point/

下面是方法的例子。

*   **例:**

    ```
    <script> 
        a = "gfg"

        b = a.codePointAt(1); 

        document.write(b + "<br>") 
    </script> 
    ```

*   **输出:**

    ```
    102
    ```

**字符串. codePointAt()** 是 JavaScript 中的一个内置方法，用于返回一个非负整数值，即给定字符串的指定元素的代码点值。
[不同元素的码点值列表:](https://en.wikipedia.org/wiki/List_of_Unicode_characters)

**语法:**

```
string.codePointAt(A)
```

**参数:**它接受一个显示字符串中某个元素索引的参数。索引从零(0)开始。

**返回值:**返回由字符串中的参数表示的元素的代码点值。如果指定位置(即第“A”个索引处)没有元素，则返回 undefined。

显示 string.codePointAt()方法工作方式的 JavaScript 代码:
**代码#1:**

```
<script>

    // Taking a string "gfg"
    a = "gfg"

    // Pointing each elements of the string
    b = a.codePointAt(0);
    c = a.codePointAt(1);
    d = a.codePointAt(2);

    // Printing the code point value of each element
    document.write(b + "<br>")
    document.write(c + "<br>")
    document.write(d)

</script>
```

**输出:**

```
103
102
103
```

**代码#2:**

```
<script>

    // Taking a string "gfg"
    a = "gfg"

    // Pointing 4th index of the string
    // index starts from 0
    b = a.codePointAt(3);

    // Printing the code point value
    document.write(b + "<br>")

</script>
```

**输出:**

```
undefined
```

**注意:**输出未定义，因为在“gfg”中第 4 个索引处没有元素。

**支持的浏览器:**

*   谷歌 Chrome 41 及以上
*   边缘 12 及以上
*   Firefox 29 及以上版本
*   歌剧 28 及以上
*   Safari 10 及以上