# JavaScript 字符串 charAt()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-charat-method/](https://www.geeksforgeeks.org/javascript-string-charat-method/)

下面是字符串 charAt()方法的例子。

*   **例:**

    ```
    <script>
    function func() {

        // Original string
        var str = 'JavaScript is object oriented language';

        // Finding the character at given index 
        var value = str.charAt(0); 
        var value1 = str.charAt(4); 
        document.write(value); 
        document.write(value1);
    }
    func();
    </script>  
    ```

*   输出:

    ```
    JS

    ```

**str.charAT()** 返回字符串给定索引处的字符。

```
character = str.charAt(index)

```

**参数:**
该函数的唯一参数是字符串中要从中提取单个字符的索引。该指标的范围在 **0** 和**长度–1**之间，包括限值。如果没有指定索引，则字符串的第一个字符返回为 **0** 是用于此功能的默认索引。

**返回值**
该函数返回位于指定为函数参数的索引处的单个字符。如果索引超出范围，则此函数返回一个空字符串。

<u>*上述功能示例如下:*</u>

**例 1:**

```
var str = 'JavaScript is object oriented language';
print(str.charAt(9));

```

输出:

```
t

```

在本例中，函数 **charAt()** 在索引 **9** 处找到字符并返回。

**例 2:**

```
var str = 'JavaScript is object oriented language';
print(str.charAt(50));

```

输出:

在本例中，函数 **charAt()** 在索引 **50** 处查找字符。由于给定字符串的索引超出范围，因此函数返回一个空字符串 **""** 。

<u>*上述功能的代码如下:*</u>

**程序 1:**

```
// JavaScript to illustrate charAt() function
<script>
function func() {

    // Original string
    var str = 'JavaScript is object oriented language';

    // Finding the character at given index 
    var value = str.charAt(9);
    document.write(value);  
}
func();
</script>  
```

输出:

```
t

```

**程序 2:**

```
<script>
// JavaScript to illustrate charAt() function
function func() {

    // Original string
    var str = 'JavaScript is object oriented language';

    // Finding the character at given index 
    var value = str.charAt(50);
    document.write(value);    
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
*   Safari 1