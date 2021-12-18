# 如何使用 JavaScript 给 HTML 元素添加/更新属性？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 向 html 元素添加-更新属性/](https://www.geeksforgeeks.org/how-to-add-update-an-attribute-to-an-html-element-using-javascript/)

我们可以使用两种方法来使用 JavaScript 修改 HTML 元素的属性。
**方法 1:**
我们可以使用 JavaScript 内置的 setAttribute()函数。
**语法:**

```
var elementVar = document.getElementById("element_id");
elementVar.setAttribute("attribute", "value");
```

所以我们基本上是通过获取元素的 id 来初始化 JavaScript 中的元素，然后使用 setAttribute()来修改它的属性。
**例:**下面是上述方法的实现。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Modify attributes method 1</title>
    <script>
        function modify() {

            //update style attribute of element "heading"

            var heading = document.getElementById("heading");
            heading.setAttribute("style", "color:green");

            //add style attribute to element "tagLine"

            var tagLine = document.getElementById("tagLine");
            tagLine.setAttribute("style", "color:blue");
        }
    </script>
</head>

<body>

    <h1 style="color:black"
        id="heading"
        align="center">
      GeeksForGeeks
  </h1>

    <p id="tagLine" align="center"> - Society Of Geeks
        <br>
        <br>
        <button onclick="modify()"> Click to modify </button>
    </p>

</body>

</html>
```

**输出:**

*   **点击按钮前:**

![](img/00a99dbdc31e1fdb31380cca8a91ca30.png)

*   **点击按钮后:**

![](img/86c66ddf85d04262985c4df98683b7ef.png)

## 方法 2:

我们甚至可以不使用 setAttribute()函数来修改 HTML 属性，如下所示:

```
document.getElementById("element_id").attribute = attribute_value;
```

**示例:**以下是上述方法的实现:

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Modify attributes method 2</title>
    <script>
        function add() {

            //get the values of fNum and sNum using getAttribute()

            var fNum = Number(document.getElementById("fNum").value);
            var sNum = Number(document.getElementById("sNum").value);
            var result = fNum + sNum;

            //output the result in green colour
            var output = "Sum of two numbers is " + result;
            document.getElementById("result").style = "color:green";
            document.getElementById("result").innerHTML = output;

            /*note the way we have updated innerHTML and added style
              attribute of "result" element */

        }
    </script>
</head>

<body>

    <h1 style="color:green" align="center">GeeksForGeeks</h1>

    <p align="center">
        <b>Enter first number :- </b>
        <input type="number" id="fNum">
        <br>
        <br>
        <b>Enter second number :- </b>
        <input type="number" id="sNum">
        <br>
        <br>
        <button onclick="add()">Add</button>
        <b><p id="result" align="center"></p>
</b>

    </p>

</body>

</html>
```

**输出:**

*   **点击按钮前:**

![](img/3bbac0ef44b47eee35f27552bae71ba0.png)

*   **点击按钮后:**

![](img/415c1ea80fac907c6d260a09269969a8.png)