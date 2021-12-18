# JavaScript 数组拼接()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-splice-method/](https://www.geeksforgeeks.org/javascript-array-splice-method/)

下面是**数组移位()**方法的例子。

**示例:**

## java 描述语言

```
<script>
    var webDvlop = ["HTML", "CSS", "JS", "Bootstrap"];

    document.write(webDvlop + "<br>");

    // Add 'React_Native' and 'Php' after removing 'JS'.
    var removed = webDvlop.splice(2, 1, 'PHP', 'React_Native')

    document.write(webDvlop + "<br>");
    document.write(removed + "<br>");

    // No Removing only Insertion from 2nd
    // index from the ending
    webDvlop.splice(-2, 0, 'React')
    document.write(webDvlop)
</script>               
```

**输出:**

```
HTML,CSS,JS,Bootstrap
HTML,CSS,PHP,React_Native,Bootstrap
JS
HTML,CSS,PHP,React,React_Native,Bootstrap
```

**arr.splice()** 方法是 JavaScript 中的内置方法，用于通过移除现有元素和/或添加新元素来修改数组的内容。

**语法:**

```
Array.splice( index, remove_count, item_list )
```

**参数:**该方法接受许多参数，其中一些参数描述如下:

*   **索引:**是必选参数。这个参数是开始修改数组的索引(原点在 0)。这也可以是负的，在许多元素从末尾开始计数之后开始。
*   **remove_count:** 要从起始索引中删除的元素数量。
*   **items_list:** 要从起始索引插入的由逗号运算符分隔的新项目列表。

**返回值:**虽然原地变异了原来的数组，但还是返回了移除项的列表。如果没有移除的数组，它将返回一个空数组。

下面的例子说明了 JavaScript 中的 Array.splice()方法:

**示例:**

## java 描述语言

```
<script>
var languages = ['C++', 'Java', 'Html', 'Python', 'C'];

document.write(languages + "<br>");

// Add 'Julia' and 'Php' after removing 'Html'.
var removed = languages.splice(2, 1, 'Julia', 'Php')

document.write(languages + "<br>");
document.write(removed + "<br>");

// No Removing only Insertion from 2nd index from the ending
languages.splice(-2, 0, 'Pascal')
document.write(languages)
</script>                   
```

**输出:**

```
C++,Java,Html,Python,C
C++,Java,Julia,Php,Python,C
Html
C++,Java,Julia,Php,Pascal,Python,C 
```

**支持的浏览器:**

*   谷歌 Chrome 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   Firefox 1 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上