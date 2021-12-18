# JavaScript | string . slice 和 String.substring 的区别

> 原文:[https://www . geesforgeks . org/JavaScript-字符串切片和字符串子字符串之间的差异/](https://www.geeksforgeeks.org/javascript-difference-between-string-slice-and-string-substring/)

这两个函数的**语法**非常相似，但在某些情况下有所不同。让我们看看它们之间的区别。

1.  **slice():**
    This method *selects the part of a string and returns the selected part as a new string*. Start and end parameters are used to specify the extracted part.
    The first character starts with index 0.

    **语法:**

    ```
    str.slice(start, end)

    ```

    **参数:**

    *   **开始:**此参数为必填项。它指定开始提取的位置。第一个字符从位置 0 开始。
    *   **结束:**此参数为可选。停止选择的位置(最多，但不包括)。如果省略参数，函数将选择从起始参数到字符串结尾的所有字符。
2.  **substring():**
    This function have the same syntax as of **slice()**
    This *method selects the part of a string and returns the selected part as a new string*. Start and end parameters are used to specify the extracted part.
    The first character starts with index 0.

    **语法:**

    ```
    str.substring(start, end)

    ```

    **参数:**

    *   **开始:**此参数为必填项。它指定开始提取的位置。第一个字符从位置 0 开始。
    *   **结束:**此参数为可选。停止选择的位置(最多，但不包括)。如果省略参数，函数将选择从起始参数到字符串结尾的所有字符。

**共同结果**
两者在给定的情况下给出相同的结果。

1.  如果`start == stop`，两者都返回一个空字符串
2.  如果省略`stop`，两者都将提取字符直到字符串结束
3.  如果任何参数大于字符串的长度，则在这种情况下将使用字符串的长度。

**子串()**
分离子串()的结果

1.  如果`start > stop`，则函数交换两个参数。
2.  如果任何参数为负或为 NaN，则视为 0。

**切片()**
切片()的单独结果

1.  如果`start > stop`，该函数将返回一个空字符串。("")
2.  如果`start`为负，它从字符串的末尾开始设置字符，如 substr()。
3.  如果`stop`为负，则设置`stop = string.length – Math.abs(stop)`(初始值)

这里有几个例子。
**示例-1:** 这两个示例在两种情况下给出了相同的结果。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript | 
      difference between String.slice and 
      String.substring
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">  
            GeeksForGeeks  
        </h1>

    <p id="GFG_UP">
    </p>

    <button onclick="Geeks()">
        click Here
    </button>

    <p id="GFG_DOWN"
       style="color:green;">
    </p>

    <script>
        var str = "This is GeeksForGeeks";
        var up = document.getElementById("GFG_UP");
        var down = document.getElementById("GFG_DOWN");
        up.innerHTML = "Str = '" + str + "'";

        function Geeks() {
            down.innerHTML = "str.slice() = "
            + str.slice(0, 13) + 
              "<br>str.substring() = "
            + str.substring(0, 13);
        }
    </script>
</body>

</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/12d1e0e80e353310dd712527aac59dd3.png)
*   **点击按钮后:**
    ![](img/8014a9a9846c3e154d93c5f5e2eae346.png)

**示例-2:** 在本例中，如果是**子字符串()**，当**开始>停止**时，它交换参数，其中**切片()**返回空字符串。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript | difference 
      between String.slice and
      String.substring
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">  
            GeeksForGeeks  
        </h1>

    <p id="GFG_UP">
    </p>

    <button onclick="Geeks()">
        click Here
    </button>

    <p id="GFG_DOWN"
       style="color:green;">
    </p>

    <script>
        var str = "This is GeeksForGeeks";
        var up = document.getElementById("GFG_UP");
        var down = document.getElementById("GFG_DOWN");
        up.innerHTML = "Str = '" + str + "'";

        function Geeks() {
            down.innerHTML = "str.slice() = "
            + str.slice(13, 0) + 
              "<br>str.substring() = "
            + str.substring(13, 0);
        }
    </script>
</body>

</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/12d1e0e80e353310dd712527aac59dd3.png)
*   **点击按钮后:**
    ![](img/906aef95d4ab73cca98be801c2db4810.png)

**示例-3:** 在本例中，在**子字符串()**的情况下，负参数被视为 0，其中**切片()**返回空字符串。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript | difference
      between String.slice and
      String.substring
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">  
            GeeksForGeeks  
        </h1>

    <p id="GFG_UP">
    </p>

    <button onclick="Geeks()">
        click Here
    </button>

    <p id="GFG_DOWN" 
       style="color:green;">
    </p>

    <script>
        var str = "This is GeeksForGeeks";
        var up = document.getElementById("GFG_UP");
        var down = document.getElementById("GFG_DOWN");
        up.innerHTML = "Str = '" + str + "'";

        function Geeks() {
            down.innerHTML = "str.slice() = "
            + str.slice(-13, 7) +
              "<br>str.substring() = "
            + str.substring(-13, 7);
        }
    </script>
</body>

</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/12d1e0e80e353310dd712527aac59dd3.png)
*   **点击按钮后:**
    ![](img/edf5bdc51c8b737433f414f7f01838eb.png)