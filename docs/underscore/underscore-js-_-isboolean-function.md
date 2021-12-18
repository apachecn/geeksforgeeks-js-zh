# 下划线. js _。isBoolean()函数

> 原文:[https://www . geesforgeks . org/下划线-js-_-isboolean-function/](https://www.geeksforgeeks.org/underscore-js-_-isboolean-function/)

下划线. js 是一个 JavaScript 库，它提供了很多有用的功能，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_isBoolean 函数**用于查找传递的元素是**真** / **假**还是**别的什么**。布尔是用于创建真/假语句的代数子集。
如果元素的值*为真或假，则输出为真*，否则输出为假。
当我们必须区分值为真或假的元素和值为非真/假的其他元素时使用。

**语法:**

```
_.isBoolean(object)
```

**参数:**
只需要一个参数，就是需要检查值的对象。

**返回值:**当对象的值为真或假时返回真，否则返回假。

1.  **Passing a variable having number value to the _.isBoolean() function:**
    The _.isBoolean() function takes the argument passed and then checks it’s value. It checks the argument’s value by comparing the value with both ‘true’ and ‘false’. If it is matched by any one of these, then output is true otherwise the output is false.
    **Example:**

    ```
    <html>

    <head>
        <script src=
    "https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
      </script>
    </head>

    <body>
        <script type="text/javascript">
            var a = 10;
            console.log(_.isBoolean(a));
        </script>
    </body>

    </html>
    ```

    **输出:**
    ![](img/c9f4eb55364a488f60fb6c2ded5b9036.png)

2.  **Passing a variable having ‘false’ as it’s value to the _.isBoolean() function:**
    If we pass an element that has ‘false’ assigned to it then also the same procedure as the previous will be followed. The argument’s value will be compared to both ‘true’ and ‘false’. Since it’s value is false, so it will be matched and hence the output will be true.
    **Example:**

    ```
    <html>

    <head>
        <script src=
    "https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
      </script>
    </head>

    <body>
        <script type="text/javascript">
            var a = false;
            console.log(_.isBoolean(a));
        </script>
    </body>

    </html>
    ```

    **输出:**
    ![](img/ac8b0c488ea2120ae4940620781cea87.png)

3.  **Passing ‘true’ to _.isBoolean() function:**
    The _.Boolean() function, in this case, does not need to check the variable’s value as no variable is passed as an argument rather the value itself is passed. The value will be matched directly to ‘true’ and ‘false’. Since the passed argument is ‘true’ so it will be matched and hence the output will be true.
    **Example:**

    ```
    <html>

    <head>
        <script src=
    "https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
      </script>
    </head>

    <body>
        <script type="text/javascript">
            console.log(_.isBoolean(true));
        </script>
    </body>

    </html>
    ```

    **输出:** ![](img/ac8b0c488ea2120ae4940620781cea87.png)

4.  **Passing ‘null’ to the _.isBoolean() function:**
    When we pass null value to the _.isBoolean() function then no error is generated rather the same checking procedure will be followed. Since after matching the null value to both the true and false, it will not be matched, so, the output will be false.
    **Example:**

    ```
    <html>

    <head>
        <script src=
    "https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
      </script>
    </head>

    <body>
        <script type="text/javascript">
            console.log(_.isBoolean(null));
        </script>
    </body>

    </html>
    ```

    **输出:** ![](img/c9f4eb55364a488f60fb6c2ded5b9036.png)

**注意:**
这些命令在 Google 控制台或 firefox 中无法工作，因为这些额外的文件需要添加，而它们没有添加。
因此，将给定的链接添加到您的 HTML 文件中，然后运行它们。
链接如下:

```
<script type=
"text/javascript" src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
</script>
```