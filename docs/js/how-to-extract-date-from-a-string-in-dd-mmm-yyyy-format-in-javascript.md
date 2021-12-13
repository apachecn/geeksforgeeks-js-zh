# 如何在 JavaScript 中从 dd-mmm-yyyy 格式的字符串中提取日期？

> 原文:[https://www . geesforgeks . org/如何从字符串中提取日期-in-DD-mmm-yyyy-format-in-JavaScript/](https://www.geeksforgeeks.org/how-to-extract-date-from-a-string-in-dd-mmm-yyyy-format-in-javascript/)

在本文中，我们将看到如何从 JavaScript 中的给定格式字符串“dd-mmm-yyyy”中提取日期。我们有一个字符串，我们想从字符串中提取日期格式“dd-mmm-yyyy”。

**示例:**

```html
// String
str = "India got freedom on 15-Aug-1947"

// Extracted date from given string in 
// "dd-mmm-yyyy" format
date = 15-Aug-1947
```

**进场:**

*   JavaScript 中没有“dd-mmm-yyyy”的原生格式。为了得到日期格式“dd-mmm-yyyy”，我们将在 JavaScript 中使用正则表达式。
*   JavaScript 中的正则表达式用于查找字符串中的模式。因此，我们将使用 match()方法在字符串中找到“dd-mmm-yyyy”模式。
*   **Syntax:**

    > str.match (/\ d {2}-(January | February | March | April | May | June | July | August | September | October | November | December)-

**示例:**

## 超文本标记语言

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">

    <meta http-equiv="X-UA-Compatible" 
        content="ie=edge">
</head>

<body>

    <!-- div element -->
    <div style="color: red;
        background-color: black;
        margin: 80px 80px;
        padding: 40px 400px;">
        India got freedom on 15-Aug-1947.

        <p></p>

        <button>
            Click the button to see date
        </button>
    </div>

    <!-- Link of JQuery cdn -->
    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js">
    </script>

    <script>

        // After clicking the button it will 
        // show the height of the div
        $("button").click(function () {

            // String that contains date
            var str = "India got freedom on 15-Aug-1947"

            // Find "dd-mmm-yyyy" format in the string
            var result =
str.match(/\d{2}-(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)-\d{4}/gi);

            // Show date on screen in 
            // format "dd-mmm-yyyy"
            $("p").html(result);
        });
    </script>
</body>

</html>
```

**点击按钮前:**

![](img/82975a8f42f587721f9632d2dfdfd41d.png)

**点击按钮后:**

![](img/cd8420ad46bfeb942c9bf15dff644d4f.png)