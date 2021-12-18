# JavaScript 错误消息属性

> 原文:[https://www . geesforgeks . org/JavaScript-error-message-property/](https://www.geeksforgeeks.org/javascript-error-message-property/)

以下是**错误消息**属性的示例。

*   **例:**

    ```
    <script>
        try {
             allert("A computer science portal");
            }
         catch(err) {
             document.write(err.message);
            }
    </script>
    ```

*   **输出:**

    ```
    allert is not defined
    ```

在 JavaScript 中，错误消息属性用于设置或返回错误消息。

**语法:**

```
errorObj.message
```

**返回值:**返回一个字符串，代表错误的详细信息。

上述属性的更多示例代码如下:

**示例 1:** 此示例不包含任何错误，因此不显示错误消息。

```
<!DOCTYPE html>
<html>
    <body style="text-align: center;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>

        <h3>
            JavaScript Error Message Property
        </h3>

        <p id="gfg"></p>

        <script>
            try {
                alert("A computer science portal");
            }
            catch(err) {
                document.getElementById("gfg").innerHTML
                        = err.message;
            }
    </script>
    </body>
</html>                    
```

**输出:**
![](img/4ff42e28dfd02ba8bfc3727147715ae8.png)

**示例 2:** 本示例在使用拼写错误的“alert”语句时显示错误消息。

```
<!DOCTYPE html>
<html>
    <body style="text-align: center;">
        <h1 style="color: green;">
            GeeksforGeeks
        </h1>

        <h3>
            JavaScript Error Message Property
        </h3>

        <p id="gfg"></p>

        <script>
            try {
                popup("A computer science portal");
            }
            catch(err) {
                document.getElementById("gfg").innerHTML
                        = err.message;
            }
        </script>
    </body>
</html>                         
```

**输出:**
![](img/5eecdc5bcfb275a7d2afd6c01446f72d.png)

**支持的浏览器:****JavaScript 错误消息属性**支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   微软公司出品的 web 浏览器
*   歌剧
*   旅行队