# JavaScript string . prototype . charcodeat()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-charcodeat/](https://www.geeksforgeeks.org/javascript-string-prototype-charcodeat/)

下面是 String.prototype.charCodeAt()方法的示例。

*   **例:**

    ```
    <script>
    function func() {
        var str = 'GEEKS';
        var value = str.charCodeAt(0);
        document.write(value);    
    }

    func();
    </script>
    ```

*   输出:

    ```
    71

    ```

**str.charCodeAt()** 方法返回一个 [Unicode 字符集](https://en.wikipedia.org/wiki/Unicode)字符的代码单元，该字符位于指定为参数的字符串的索引处。该方法的语法如下:

```
str.charCodeAt(index)

```

**参数**
这个方法的唯一参数是字符串中要使用 Unicode 的字符的索引。指数范围从 **0** 到**长度–1**。

**返回值**
该方法返回字符的 Unicode(范围在 0 到 65535 之间)，该字符的索引作为参数提供给该方法。如果提供的指数超出范围，该方法返回 **NaN** 。

<u>*上述方法示例如下:*</u>

**例 1:**

```
Input:
var str = 'ephemeral';
print(str.charCodeAt(4));

Output:
109

```

在本例中，方法 **charCodeAt()** 从索引 **4** 处的字符串中提取字符。由于该字符是 **m** ，因此该方法返回的 Unicode 序列为 **109** 。

**例 2:**

```
Input:
var str = 'ephemeral';
print(str.charCodeAt(20));

Output:
NaN

```

在本例中，方法 **charCodeAt()** 从索引 **20** 处的字符串中提取字符。由于该字符串的索引超出范围，因此该方法返回的答案为 **NaN** 。

<u>*上述方法的代码如下:*</u>

**程序 1:**

```
<script>
// JavaScript to illustrate charCodeAt() method

function func() {
    var str = 'ephemeral';

    // Finding the code of the character at
    // given index 
    var value = str.charCodeAt(4);
    document.write(value);    
}

func();
</script>
```

输出:

```
109

```

**程序 2:**

```
<script>
// JavaScript to illustrate charCodeAt() method

function func() {
    var str = 'ephemeral';

    // Finding the code of the character 
    // at given index 
    var value = str.charCodeAt(20);

    document.write(value);    
}
func();
</script> 
```

输出:

```
NaN

```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   safari 1 及以上
*   歌剧 4 及以上