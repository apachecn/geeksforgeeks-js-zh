# Javascript Number()函数

> 原文:[https://www.geeksforgeeks.org/javascript-number-function/](https://www.geeksforgeeks.org/javascript-number-function/)

下面是 **Number()函数**的例子。

*   **例:**

    ```
    <script>
        // JavaScript to illustrate
        // Number() function
        function func() {

            // Original string
            var a = true;

            var value = Number(a);
            document.write(value);
        }
    // Driver code
    func();
    </script> 
    ```

*   **输出:**

    ```
    1
    ```

**Number()** 功能用于将数据类型转换为数字。

**语法:**

```
Number(object)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

**对象:**此参数保存将任何类型的 javascript 变量转换为数字类型的对象。

**返回值:** Number()函数返回任意类型 javascript 变量的数字格式。

下面的例子说明了 JavaScript 中的 Number()函数:

*   **例 1:**

    ```
    Input : Number(true);
                 Number(false);
    Output : 1
             0
    ```

*   **示例 2:** 编译器没有返回任何数字。

    ```
    Input : Number("10 20");
    Output: NaN
    ```

*   **示例 3:** 上面的 **Number()** 方法返回自 1970 年 1 月 1 日以来的毫秒数。

    ```
    Input : Number(new Date("2017-09-30"));
    Output : 1506729600000
    ```

*   **例 4:**

    ```
    Input : Number("John");
    Output : NaN

    ```

上述功能的更多示例代码如下:

**程序 1:**

```
<script>
    // JavaScript to illustrate Number() function
    function func() {

        // Original string
        var a = "10 20";

        var value = Number(a);
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

**程序 2:**

```
<script>
    // JavaScript to illustrate Number() function
    function func() {
        var value = Number(new Date("2017-09-30"));
        document.write(value);
    }
// Driver code
func();
</script>
```

**输出:**

```
1506729600000
```

**程序 4:**

```
<script>
    // JavaScript to illustrate Number() function
    function func() {
        var value = Number("John");
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
*   火狐浏览器
*   微软公司出品的 web 浏览器
*   旅行队
*   歌剧