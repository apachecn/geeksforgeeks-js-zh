# 如何检查一个 JavaScript 对象是不是 DOM 对象？

> 原文:[https://www . geesforgeks . org/how-check-a-JavaScript-object-is-DOM-object/](https://www.geeksforgeeks.org/how-to-check-a-javascript-object-is-a-dom-object/)

**先决条件:** [DOM(文档对象模型)](https://www.geeksforgeeks.org/dom-document-object-model/)[运算符实例](https://www.geeksforgeeks.org/instanceof-operator-in-javascript/)

**DOM(Document Object Model):**Document Object Model 是 HTML 和 XML 文档的分层表示，其格式在编程方面更容易解释。它通过以由节点组成的树状模型的形式解释其结构来操纵标签、元素、属性和类。

**元素:**在 HTML DOM 中，*元素*是所有对象的通用基类。一个元素对象代表所有的 HTML 元素。

**方法:**为了检查一个 JavaScript 对象是否是 DOM 对象，我们需要检查给定的 JS 对象是否是*元素*类型的对象。为了检查这一点，我们将使用运算符的**实例。instanceof 运算符返回一个布尔值，该值指定对象是否是给定类的实例。**

**语法:**

```html
Object instanceof ObjectType
```

**参数:**

*   **对象:**存储需要测试的对象。
*   **对象类型:**它存储要测试的对象类型。

**示例:**

```html
<!DOCTYPE HTML> 
<html> 

<head> 
    <title>
        How to check a JavaScript 
        Object is a DOM Object ?
    </title>
</head>

<body>
    <div id="div1"></div> 
    <div id="nonElem"></div> 

    <script>
        // Function to check the object
        // id DOM object or not
        function isDOM(Obj) {

             // Function that checks whether 
             // object is of type Element
            return Obj instanceof Element;
        }

        // Set all elements into HTML
        var div = document.getElementById('div1');
        var nonElem = document.getElementById('nonElem');

        // Creating a non-DOM Object 
        var x = 1; 

        // Checks against HTML elements and
        // non-HTML elements
        if (isDOM(div))
            div.innerHTML = "Div is detected as a DOM Object";

        if (!isDOM(x)) 
            nonElem.innerHTML = "x is detected as a non-DOM Object"; 
    </script>
</body>

</html>
```

**输出:**

```html
Div is detected as a DOM Object
x is detected as a non-DOM Object

```