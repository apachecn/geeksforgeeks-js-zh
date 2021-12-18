# JavaScript 字符串开始用()方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-startswith/](https://www.geeksforgeeks.org/javascript-string-startswith/)

下面是 String startsWith()方法的示例。

*   **例:**

## Java Script 语言

```
<script>
function func() {
    var str = 'Geeks for Geeks';
    var value = str.startsWith('Gee');
    document.write(value);
}
func();
</script>
```

*   **输出:**

```
true
```

**str.startsWith()** 方法用于检查给定字符串是否以指定字符串的字符开始。
**语法:**

```
str.startsWith( searchString , position )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **searchString:** 必选参数。它存储需要搜索的字符串。
*   **start:** 它确定给定字符串中搜索字符串的位置。默认值为零。

**返回值**如果找到搜索字符串，该方法返回布尔值**真**，否则返回**假**。
上述方法的示例如下:
**示例 1:**

```
var str = 'It is a great day.';
var value = str.startsWith('It'); 
print(value);
```

**输出:**

```
true
```

在上例中，方法 **startsWith()** 检查字符串 **str** 是否以 **It** 开头。由于字符串以**开始，因此它返回**真**。
**例 2:**** 

```
var str = 'It is a great day.';
var value = str.startsWith('great');
print(value);
```

**输出:**

```
false
```

在本例中，方法**以()**开始，检查字符串**字符串**是否以**开头。由于**大**出现在弦的中间而不是开始，因此它返回**假**。
**例 3:**** 

```
var str = 'It is a great day.'
var value = str.startsWith('great',8);
print(value);
```

**输出:**

```
true
```

在本例中，方法
**start with()**检查字符串 **str** 是否在指定的索引 **8** 处以**开头。由于**极大**出现在字符串的给定索引处，因此它返回**真**。
以下程序说明了 JavaScript 中的 startsWith()方法:
**程序 1:**** 

## Java Script 语言

```
<script>
// JavaScript to illustrate startsWith() method

function func() {

    // Original string
    var str = 'It is a great day.';

    // Checking the condition
    var value = str.startsWith('It');
    document.write(value);
}
func();
</script>
```

**输出:**

```
true
```

**节目 2:**

## Java Script 语言

```
<script>

// JavaScript to illustrate
// startsWith() method
function func() {

    // Original string
    var str = 'It is a great day.';
    var value = str.startsWith('great');
    document.write(value);
}
func();
</script>
```

**输出:**

```
false
```

**节目 3:**

## Java Script 语言

```
<script>

// JavaScript to illustrate
// startsWith() method
function func() {

    // Original string
    var str = 'It is a great day.';
    var value = str.startsWith('great', 8);
    document.write(value);
}

// Function call
func();

</script>
```

**输出:**

```
true
```

**支持的浏览器:**

*   Chrome 41 及以上
*   边缘 12 及以上
*   歌剧 28 及以上
*   Firefox 17 及以上版本
*   Safari 9 及以上