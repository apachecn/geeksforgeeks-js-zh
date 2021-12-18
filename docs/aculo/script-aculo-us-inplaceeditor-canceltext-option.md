# 脚本. aculo . us in place editor cancel text option

> 原文:[https://www . geesforgeks . org/script-aculo-us-in placeeditor-canceltext-option/](https://www.geeksforgeeks.org/script-aculo-us-inplaceeditor-canceltext-option/)

script.aculo.us 库是一个跨浏览器库，旨在改进网站的用户界面。Ajax。InPlaceEditor 用于使元素可编辑，从而允许用户编辑页面上的内容并将更改提交给服务器。

位置编辑器中的**取消文本**选项用于指定取消编辑并关闭编辑器的链接文本。该选项的默认字符串值是“取消”。

**语法:**

```
{ cancelText : string }
```

**值:**该选项具有如上所述的单个值，如下所述:

*   **字符串:**这是一个字符串，指定要为用于取消编辑的链接显示的文本。默认字符串是“取消”。

以下示例说明了该选项的使用。

**示例:**下面的 HTML 文件演示了 InPlaceEditor cancelText 选项示例。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript"
        src="prototype.js">
    </script>

    <script type="text/javascript"
        src="scriptaculous.js?load = controls">
    </script>

    <script type="text/javascript">
        window.onload = function () {

            // Default InPlaceEditor with no
            // options
            new Ajax.InPlaceEditor(
                'editableElement',
                'http://localhost/tmpscripts/inplace.php',
            );

            // InPlaceEditor where the
            // cancelText option is modified
            new Ajax.InPlaceEditor(
                'editableElement2',
                'http://localhost/tmpscripts/inplace.php',
                {

                    // Specify the text to be used for
                    // the link to cancel the edit
                    cancelText: "Press to cancel!"
                }
            );
        }
    </script>
</head>

<body>
    <h1 style="color: green">
        GeeksforGeeks
    </h1>

    <h2>InPlaceEditor cancelText Option</h2>

<p>
        The "cancelText" option is used to
        specify the text to be shown for the
        cancel option of the editor.
    </p>

    <b>
        This element has the cancelText
        as the default one.
    </b>

    <div id="editableElement">
        Click this element to edit it!
    </div>
    <br>

    <b>
        This element has the cancelText
        set to a custom value.
    </b>

    <div id="editableElement2">
        Click this element to edit it!
    </div>
</body>

</html>
```

下面的 PHP 文件演示了这个例子:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
  if( isset($_REQUEST["value"]) ) {
    $str = $_REQUEST["value"];
    echo $str;
  }
?>
```

**输出:**

![](img/4486d242c863c7eaaed41f9c70dae54f.png)