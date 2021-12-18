# JavaScript 字符串 substr()方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-substr/](https://www.geeksforgeeks.org/javascript-string-substr/)

下面是字符串 substr()方法的示例。

*   **例:**

## Java Script 语言

```
<script>
function func() {
    var str = 'Geeks for Geeks';
    var sub_str = str.substr(6);
    document.write(sub_str);
}
func();
</script>
```

*   输出:

```
for Geeks
```

**str.substr()** 方法从给定字符串的指定索引中返回指定数量的字符。
**语法:**

```
str.substr(start , length)
```

*   **start:** 定义从基串中提取子串的起始索引。
*   **长度:**定义从给定字符串中的**开始**开始提取的字符数。如果函数的第二个参数未定义，则从**开始到长度结束的所有字符都将被提取。**

**返回值:**
这个方法返回一个字符串，它是给定字符串的一部分。如果**长度**为 **0** 或负值，则返回空字符串。
*<u>上述方法的示例如下:</u>*
**示例 1:**

```
var str = 'It is a great day.'
print(str.substr(5));
```

输出:

```
 a great day.
```

在本例中，方法 **substr()** 创建一个从索引 **5** 开始直到字符串结束的子字符串。
**例 2:**

```
var str = 'It is a great day.'
print(str.substr(5,6));
```

输出:

```
 a gre
```

在本例中，方法 **substr()** 从索引 **5** 开始提取子字符串，字符串长度为 **6** 。
**例 3:**

```
var str = 'It is a great day.'
print(str.substr(5,-7));
```

输出:

在本例中，由于要提取的字符串长度为负，因此该方法返回一个空字符串。
*<u>上述方法的代码如下:</u>*
**程序 1:**

## Java Script 语言

```
<script>
// JavaScript to illustrate substr() function

function func() {

    // Original string
    var str = 'It is a great day.';
    var sub_str = str.substr(5);
    document.write(sub_str);
}

func();
</script>
```

输出:

```
 a great day.
```

**节目 2:**

## Java Script 语言

```
<script>
// JavaScript to illustrate substr() function

function func() {

    // Original string
    var str = 'It is a great day.';

    var sub_str = str.substr(5,6);
    document.write(sub_str);
}

func();
</script>
```

输出:

```
 a gre
```

**节目 3:**

## Java Script 语言

```
<script>
// JavaScript to illustrate substr() function

function func() {

    // Original string
    var str = 'It is a great day.';

    var sub_str = str.substr(5,-7);
    document.write(sub_str);
}
func();
</script>
```

输出:

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上