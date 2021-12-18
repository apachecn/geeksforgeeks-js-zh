# 下划线. js _。isArray()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-isarray-function/](https://www.geeksforgeeks.org/underscore-js-_-isarray-function/)

下划线. js 是一个 JavaScript 库，它提供了很多有用的功能，比如映射、过滤、调用等，甚至不使用任何内置对象。

_。isArray()函数用于查找传递的参数是否为数组。数组是一组变量、常数和特殊符号。如果对象是数组，将返回 True，否则将返回 false。数组可以有不同的名称，并且可以是任何大小，甚至是零。

**语法:**

```
_.isArray(object)
```

**参数:**
只需要一个参数，即需要检查的对象。

**返回值:**
如果传递的参数是数组，则返回“真”，否则返回“假”。

1.  **Passing an array of 3 numbers to the _.isArray() function:**
    The _.isArray() function takes the element passed and checks whether it is an array or not. Since the passed argument is a set of 3 numbers – 1, 2, 3\. Therefore, it is an array. And Hence, the final output will be true.
    **Examples:**

    ```
    <html>

    <head>
        <script src=
    "https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
      </script>
    </head>

    <body>
        <script type="text/javascript">
            console.log(_.isArray([1, 2, 3]));
        </script>
    </body>

    </html>
    ```

    **输出:**
    ![](img/ac8b0c488ea2120ae4940620781cea87.png)

2.  **Passing an array of characters to the _.isArray() function:**
    The argument passed to the _.isArray() function will be checked that is it an array or not. Since the argument is containing only one character, “a” but is inside [] brackets so it is an array. And hence the answer is true.
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
            console.log(_.isArray(["a"]));
        </script>
    </body>

    </html>
    ```

    **输出:**
    ![](img/ac8b0c488ea2120ae4940620781cea87.png)

3.  **Passing an empty array to _.isArray() function:**
    The _.isArray() function takes the element which here is [] and then checks whether it is an array or not. Since there is not element inside the [] brackets so, it is empty. But since [] brackets are present so it is an array. Since empty array is also an array so the output is true.
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
            console.log(_.isArray([]));
        </script>
    </body>

    </html>
    ```

    **输出:**
    ![](img/ac8b0c488ea2120ae4940620781cea87.png)

4.  **Passing a number to the _.isArray() function:**
    If we pass any random number to the _.isArray() function then as it will check that the argument is an array or not. Since, a number is passed to the _.isArray() function therefore the output will be false.
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
            console.log(_.isArray(1));
        </script>
    </body>

    </html>
    ```

    **输出:**
    ![](img/c9f4eb55364a488f60fb6c2ded5b9036.png)

    `

**注意:**
这些命令在 Google 控制台或 firefox 中无法工作，因为这些额外的文件需要添加，而它们没有添加。
因此，将给定的链接添加到您的 HTML 文件中，然后运行它们。链接如下:

```
<script type="text/javascript" src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
</script>
```