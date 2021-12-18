# script . aculo . us in placeeditor external control 选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-in placeeditor-external control-option/](https://www.geeksforgeeks.org/script-aculo-us-inplaceeditor-externalcontrol-option/)

在本文中，我们将通过使用名为 **script.aculo.us** 的 JavaScript 库来演示 **InPlaceEditor** 类的 **externalControl** 选项的效果，该库帮助我们添加一个元素，该元素将触发就地编辑器的编辑。

**语法:**

```
Ajax.InPlaceEditor( element, url, { size: 100 });
```

**方法 1:** 为了演示这个函数的使用，我们编写了一小段代码。我们已经编写了一个小的 JavaScript 代码，它将为特定的元素创建一个就地编辑器。通过点击按钮，您将看到原位编辑器被触发并进入编辑模式。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Import the libraries -->
    <script type="text/javascript"
        src="prototype.js">
    </script>

    <script type="text/javascript"
        src="scriptaculous.js">
    </script>
</head>

<body>
    <p id="editme">Click me</p>

    <button id="editbutton">
        Edit
    </button>

    <!-- Script for the JavaScript
        to initialize the objects -->
    <script type="text/javascript">
        new Ajax.InPlaceEditor(
            'editme', 'example', 
            { externalControl: 'editbutton' }
        );
    </script>
</body>

</html>
```

**输出:**

![](img/c490a006e6d0277b942be3c5444afac6.png)

**方法 2:** 在这种方法中，我们编写了一个小的 JavaScript 代码，它将为特定的元素创建一个就地编辑器，然后我们将向一个文件发出请求，并从该文件中获取内容。我们将创建一个名为*test.html*的文件，其中有一个简单的文本 **GeeksforGeeks** 。点击按钮，你会看到就地编辑器被触发，进入编辑模式，我们会点击*确定*从文件中获取内容。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Import the libraries -->
    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
        src="scriptaculous.js">
    </script>
</head>

<body>
    <p id="editme">Click me</p>

    <button id="editbutton">
        Edit
    </button>

    <!-- Script to initialize the objects -->
    <script type="text/javascript">
        new Ajax.InPlaceEditor(
            'editme', '/test.html', 
            { externalControl: 'editbutton' }
        );
    </script>
</body>

</html>
```

**输出:**

![](img/921dbe9026446c63f3f3f5b6c3623641.png)