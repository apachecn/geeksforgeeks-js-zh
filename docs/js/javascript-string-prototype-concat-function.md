# JavaScript 字符串 concat()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-concat-function/](https://www.geeksforgeeks.org/javascript-string-prototype-concat-function/)

下面是 concat()方法的示例。

*   **例:**

    ```
    <script> 
    // JavaScript to illustrate concat() function 
    function func() { 

        // Original string 
        var str = 'Geeks'; 

        // Joining the strings together 
        var value = str.concat(' for',' Geeks'); 
        document.write(value);     
    } 
    func(); 
    </script> 
    ```

*   输出:

    ```
    Geeks for Geeks

    ```

**str.concat()** 函数用于在 JavaScript 中将两个或多个字符串连接在一起。

**语法:**

```
str.concat(string2, string3, string4,......, stringN)
```

**参数:**
这个函数的参数是需要连接在一起的字符串。此函数的参数数量等于要连接在一起的字符串数量。

**返回值:**
这个函数返回一个新的字符串，它是作为参数传递给它的所有不同字符串的组合。

<u>*上述功能示例如下:*</u>

**例 1:**

```
print('It'.concat(' is',' a',' great',' day.'));

```

输出:

```
It is a great day.

```

在本例中，函数 **concat()** 将**【它】**与**连接在一起，是“**、**“a”**、**“伟大”**、**“天”**创建包含所有字符串的最终字符串。

<u>*上述功能的代码如下:*</u>

**程序 1:**

```
<script>
// JavaScript to illustrate concat() function
function func() {

    // Original string
    var str = 'It';

    // Joining the strings together
    var value = str.concat(' is',' a',' great',' day.');
    document.write(value);    
}
func();
</script> 
```

输出:

```
It is a great day.

```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上