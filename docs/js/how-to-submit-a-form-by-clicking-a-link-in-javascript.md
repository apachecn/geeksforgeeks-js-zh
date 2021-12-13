# 如何在 JavaScript 中点击链接提交表单？

> 原文:[https://www . geesforgeks . org/如何通过单击 javascript 中的链接提交表单/](https://www.geeksforgeeks.org/how-to-submit-a-form-by-clicking-a-link-in-javascript/)

在本文中，我们通过点击一个链接，使用 [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) 提交了一个表单。在正文标签中，创建了一个 HTML 表单，并指定了[表单](https://www.geeksforgeeks.org/html-design-form/)的 id、方法和动作。在表格中，用事件[点击](https://www.geeksforgeeks.org/html-onclick-event-attribute/)指定一个[锚点](https://www.geeksforgeeks.org/html-links/)标签。为 JavaScript 创建一个[函数](https://www.geeksforgeeks.org/functions-in-javascript/)，当点击链接时将被执行。当我们点击链接时，函数 submitForm()将被执行。该函数将表单 Id 传递给 DOM [getElementById()](https://www.geeksforgeeks.org/html-dom-getelementbyid-method/) 方法获取元素对象，然后使用 [submit()](https://www.geeksforgeeks.org/html-dom-form-submit-method/) 方法提交表单。

**示例:**使用上述方法创建表单并提交。这是用户提供其详细信息的表单结构所必需的。

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<body>
    <h2 style="color:green">GeeksforGeeks</h2>
    <b>Submit form details</b>

    <form id="form__submit" action="form.php" method="post">
        <label>NAME: </label><br />
        <input type="text" name="name" /><br />
        <label>AGE: </label><br />
        <input type="number" name="age" /><br />
        <label>CITY: </label><br />
        <input type="text" name="city" /><br /><br />
        <a href="#" onclick="submitForm()">Submit Here</a>
    </form>

    <script>
        function submitForm() {
            let form = document.getElementById("form__submit");
            form.submit();
        }
    </script>
</body>

</html>
```

**注意:**给定的 HTML 代码会将表单数据重定向到 [**动作**](https://www.geeksforgeeks.org/html-action-attribute/) 属性中提到的站点或文件。

**PHP 代码:**创建一个 PHP 文件获取用户输入的表单数据，将这个 PHP 文件重命名为“form.php”。此代码显示用户表单数据。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```html
<?php
    $name=$_POST['name'];
    $age=$_POST['age'];
    $city=$_POST['city'];

    echo "NAME-SUBMITTED : $name <br>";

    echo "AGE-SUBMITTED :  $age <br>";

    echo "CITY-SUBMITTED:  $city";
?>
```

**输出:**

![](img/aeaae278993ce7bc39202a44d08c1347.png)

用户表单数据

PHP 是一种客户端语言。所以它需要一个服务器。请参考 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)更好的理解。