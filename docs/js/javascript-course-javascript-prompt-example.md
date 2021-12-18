# JavaScript 课程| JavaScript 提示示例

> 原文:[https://www . geesforgeks . org/JavaScript-课程-JavaScript-提示-示例/](https://www.geeksforgeeks.org/javascript-course-javascript-prompt-example/)

**前题:** [JavaScript 课程| JavaScript 中的条件运算符](https://www.geeksforgeeks.org/javascript-course-conditional-operator-in-javascript/)
现在我们知道如何通过提示、提醒和确认与用户进行交互了。让我们构建一个纯粹使用普通 Javascript 编写的简单应用程序，在这个程序中，我们询问用户的姓名和年龄，然后利用我们到目前为止所学的运算符和条件语句来检查他/她是否应该被允许进入“La La Land！”。
**使用的工具**

*   Visual Studio 代码
*   Mozilla Firefox

**注意:**任何浏览器都可以，不过推荐谷歌 Chrome 或者 Mozilla firefox。
T3】项目结构 T5】

```
  prompt-example  // name of the folder
   --index.html
   --app.js
```

index.html 文件将包含我们将呈现的简单 HTML 内容，app.js 文件是我们将在其中编写 javascript 代码的 javascript 文件。
**index.html 文件**T3】

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8"> <!-- character encoding -->
   <!-- setting the default width to devices width -->
  <meta name="viewport" content="width=device-width">
   <!-- optional --> 
  <meta name="author" content="Mukul-Latiyan">
  <title>Prompt Example</title>
    <!-- external package -->
    <script src="https://unpkg.com/sweetalert/dist/sweetalert.min.js">
    </script>
</head>
<body>
   <!-- simple h1 heading -->
   <h1 style="text-align:center";>Prompt example!</h1>
   <!-- linking the javascript file -->
   <script src="app.js"></script>
</body>
</html>
```