# JavaScript 字符串 indexOf()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-indexof-function/](https://www.geeksforgeeks.org/javascript-string-prototype-indexof-function/)

下面是()方法的字符串索引示例。

*   **示例:**

## Java Script 语言

```
// JavaScript to illustrate indexOf() function
<script>
function func() {

    // Original string
    var str = 'Departed Train';

    // Finding index of occurrence of 'Train'
    var index = str.indexOf('Train');
    document.write(index);
}
func();
</script>
```

*   输出:

```
9
```

**str.indexOf()** 函数查找给定字符串中参数字符串第一次出现的索引。返回值从 0 开始。该函数的语法如下:

```
str.indexOf(searchValue , index)
```

**参数:**
函数的第一个参数**搜索值**是要在基本字符串中搜索的字符串。函数**索引**的第二个参数定义了起始索引，从该索引开始在基本字符串中搜索**搜索值**。

**返回值:**
该函数返回第一次找到**搜索值**的字符串的索引(从 0 开始)。如果在字符串中找不到**搜索值**，则该功能返回 **-1** 。
*<u>上述功能示例如下:</u>*
**示例 1:**

```
print('Departed Train'.indexOf('Train')); 
```

在本例中，函数 **indexOf()** 找到字符串 **Train** 的索引。由于第一个也是唯一一个存在该字符串的索引是 9，因此该函数返回 **9** 作为答案。

输出:

```
9
```

**例 2:**

```
print('Departed Train'.indexOf('ed Tr')); 
```

输出:

```
6
```

在本例中，函数 **indexOf()** 找到字符串 **ed Tr** 的索引。由于该字符串出现的第一个也是唯一一个索引是 6，因此该函数返回 **6** 作为答案。
**例 3:**

```
print('Departed Train'.indexOf('train')); 
```

输出:

```
-1
```

在本例中，函数 **indexOf()** 找到字符串 **Train** 的索引。由于字符串中不存在**搜索值**，因此该函数返回 **-1** 作为答案。
**例 4:**

```
print('Departed Train before another Train'.indexOf('Train')); 
```

输出:

```
9
```

在本例中，函数 **indexOf()** 找到字符串 **Train** 的索引。由于**搜索值**的第一个索引是 **9** ，因此该函数返回 **9** 作为答案。
*<u>上述功能的代码如下:</u>*
**程序 1:**

## Java Script 语言

```
// JavaScript to illustrate indexOf() function
<script>
function func() {

    // Original string
    var str = 'Departed Train';

    // Finding index of occurrence of 'Train'
    var index = str.indexOf('Train');
    document.write(index);
}
func();
</script>
```

输出:

```
9
```

**程序 2:**

## Java Script 语言

```
<script>
// JavaScript to illustrate indexOf() function
function func() {

    // Original string
    var str = 'Departed Train';

    // Finding index of occurrence of 'Train'
    var index = str.indexOf('ed Tr');
    document.write(index); 
}
func();
</script> 
```

输出:

```
6
```

**程序 3:**

## Java Script 语言

```
// JavaScript to illustrate indexOf() function
<script>
function func() {

    // Original string
    var str = 'Departed Train';

    // Finding index of occurrence of 'Train'
    var index = str.indexOf('train');
    document.write(index); 
}
func();
</script> 
```

输出:

```
-1
```

**程序 4:**

## Java Script 语言

```
// JavaScript to illustrate indexOf() function
<script>
function func() {

    // Original string
    var str = 'Departed Train before another Train';

    // Finding index of occurrence of 'Train'
    var index = str.indexOf('Train');
    document.write(index); 
}
func();
</script> 
```

输出:

```
9 
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上