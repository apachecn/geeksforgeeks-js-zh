# Javascript eval()函数

> 原文:[https://www.geeksforgeeks.org/javascript-eval-function/](https://www.geeksforgeeks.org/javascript-eval-function/)

下面是 **eval()函数**的例子。

*   **例:**

    ```
    <script>
        // JavaScript to illustrate eval() function
        function func() {

            // Original string
            var a = 4;
            var b = 4;

            // Finding the multiplication
            var value = eval(new String(a * b));
            document.write(value);
        }
    // Driver code
    func();
    </script>                    
    ```

*   **输出:**

    ```
    16
    ```

**eval()** 函数用于计算表达式。如果该参数表示一个或多个 JavaScript 语句，则 **eval()** 会计算这些语句。我们不使用 **eval()** 来计算算术表达式。JavaScript 自动计算算术表达式。

**语法:**

```
eval(string)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **字符串:**表示 JavaScript 表达式、语句或语句序列的字符串。表达式可以包括现有对象的变量和属性。

**返回值:**使用 **eval()** 返回评估给定代码的完成值。如果完成值为空，则返回**未定义的**。

下面的例子说明了 JavaScript 中的 **eval()函数**:

**例 1:**

```
Input : eval(new String('2 + 2'));
Output: returns a String object containing "2 + 2"
```

```
Input : eval(new String('4 + 4'));
Output: returns a String object containing "4 + 4"
```

以上功能的更多示例代码如下:
**程序 1:**

```
<script>
    // JavaScript to illustrate eval() function
    function func() {

        // Original string
        var a = 2;
        var b = 2;

        // Finding the sum
        var value = eval(new String(a + b));
        document.write(value);
    }
// Driver Code
func();
</script>                    
```

**输出:**

```
4
```

**程序 2** :

```
<script>
    // JavaScript to illustrate eval() function
    function func() {

        // Original string
        var a
        var b

        // Finding the Sumation
        var value = eval(new String(a + b));
        document.write(value);
    }
// Driver code
func();
</script>                
```

**输出:**

```
NaN
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   Mozilla Firefox
*   旅行队
*   歌剧