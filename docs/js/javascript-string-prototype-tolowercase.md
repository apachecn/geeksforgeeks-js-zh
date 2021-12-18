# JavaScript 字符串 toLowerCase()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-tolowercase/](https://www.geeksforgeeks.org/javascript-string-prototype-tolowercase/)

下面是字符串 toLowerCase()方法的示例。

*   **例:**

## Java Script 语言

```
<script>
function func() {
    var str = 'GEEKSFORGEEKS';
    var string = str.toLowerCase();
    document.write(string);
}
func();
</script>
```

*   输出:

```
geeksforgeeks
```

**str.toLowerCase()** 方法将整个字符串转换为小写。该方法不影响任何特殊字符、数字和小写字母。
**语法:**

```
str.toLowerCase()
```

**返回值:**
这个方法返回一个新的字符串，其中所有大写字母都转换成小写。
*<u>上述方法的示例如下:</u>*
**示例 1:**

```
var str = 'It iS a Great Day.';
var string = str.toLowerCase();
print(string);
```

输出:

```
it is a great day.
```

在本例中，方法 **toLowerCase()** 将所有大写字母转换为小写字母，而不影响特殊字符、数字和所有那些已经是小写的字符。
**例 2:**

```
var str = 'It iS a 5r&e@@t Day.';
var string = str.toLowerCase();
print(string);
```

输出:

```
it is a 5r&e@@t day.
```

在本例中，方法 **toLowerCase()** 将所有大写字母转换为小写字母，而不影响特殊字符、数字和所有已经小写的字符。
*<u>上述方法的代码如下:</u>*
**程序 1:**

## Java Script 语言

```
<script>
// JavaScript Program to illustrate
//  toLowerCase() method

function func() {

    // Original string
    var str = 'It iS a Great Day.';

    // Converting to lower case
    var string = str.toLowerCase();
    document.write(string);
}

func();
</script>
```

输出:

```
it is a great day.
```

**节目 2:**

## Java Script 语言

```
<script>
// JavaScript Program to illustrate
//  toLowerCase() method

function func() {

    //Original string
    var str = 'It iS a 5r&e@@t Day.';

    //Converting to lower case
    var string = str.toLowerCase();
    document.write(string);
}

func();
</script>
```

输出:

```
it is a 5r&e@@t day.
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上