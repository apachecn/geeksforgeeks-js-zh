# 如何在 JavaScript / jQuery 中更改 img 元素的 src 属性？

> 原文:[https://www . geesforgeks . org/如何更改 javascript-jquery/](https://www.geeksforgeeks.org/how-to-change-the-src-attribute-of-an-img-element-in-javascript-jquery/) 中 img 元素的-src-attribute

任务是使用 JQuery 和 JavaScript 更改元素的 src 属性。

*   **jQuery prop() Method:** This method set/return properties and values of the matched elements. If this method is used to return the property value, it returns the value of the first selected element. If this method is used to set property values, it sets one or more property/value pairs for the set of selected elements.

    **语法:**

    *   **返回一个属性的值:**

        ```
        $(selector).prop(property)
        ```

    *   **设置属性和值:**

        ```
        $(selector).prop(property, value)
        ```

    *   **使用函数设置属性和值:**

        ```
        $(selector).prop(property, function(index, currentvalue))
        ```

    *   **设置多个属性和值:**

        ```
        $(selector).prop({property:value, property:value, ...})
        ```

    **参数:**

    *   **属性:**此参数指定属性的名称。
    *   **值:**此参数指定属性的值。
    *   **函数(索引，currentvalue):** 此参数指定一个返回要设置的属性值的函数。
        *   **索引:**该参数接收集合中元素的索引位置。
        *   **当前值:**此参数接收选定元素的当前属性值。
*   **jQuery on() Method:** This method adds one or more event handlers for the selected elements and child elements.

    **语法:**

    ```
    $(selector).on(event, childSelector, data, function, map)
    ```

    **参数:**

    *   **事件:**此参数为必填项。它指定一个或多个要附加到选定元素的事件或命名空间。如果有多个事件值，这些值用空格隔开。事件必须是有效的。
    *   **儿童选择器:**该参数可选。它指定事件处理程序应该只附加到已定义的子元素。
    *   **数据:**此参数为可选。它指定要传递给函数的附加数据。
    *   **功能:**此参数为必选项。它指定事件发生时要运行的函数。
    *   **映射:**它指定了一个事件映射({event:func()，event:func()，…})，该事件映射有一个或多个要添加到所选元素的事件，以及事件发生时要运行的函数。

**示例 1:** 本示例使用 JavaScript 更改图像的 src 属性。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            Change the src attribute
            of an img tag
        </title>     
    </head> 

    <body style = "text-align:center;"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <p id = "GFG_UP" style =
            "font-size: 15px; font-weight: bold;">
        </p>

        <img id = "img" src =
"https://media.geeksforgeeks.org/wp-content/uploads/20190529122828/bs21.png" />

        <br>

        <button onclick = "GFG_Fun()">
            click here
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script> 
            var up = document.getElementById('GFG_UP');
            up.innerHTML = "Click on button to change the src of image";
            var down = document.getElementById('GFG_DOWN'); 

            function GFG_Fun() {
                document.getElementById("img").src =
'https://media.geeksforgeeks.org/wp-content/uploads/20190529122826/bs11.png';
                down.innerHTML = "src attribute changed";
            }
        </script> 
    </body> 
</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/d58925d4707880484092e8cf98c110c3.png)
*   **点击按钮后:**
    ![](img/c0a9e57260264e76c70ab3fe519ffdd2.png)

**示例 2:** 本示例使用 JQuery 更改图像的 src 属性。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            Change the src attribute of
            an img tag using jQuery
        </title>

        <script src =
"https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js">
        </script>
    </head> 

    <body style = "text-align:center;">

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <p id = "GFG_UP" style = 
            "font-size: 15px; font-weight: bold;">
        </p>

        <img id = "img" src =
"https://media.geeksforgeeks.org/wp-content/uploads/20190529122828/bs21.png" />

        <br>

        <button onclick = "GFG_Fun()">
            click here
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script> 
            $("#GFG_UP").text("Click on button to change the src of image");
            $('button').on('click', function(e) {
                $('#img').prop('src',
'https://media.geeksforgeeks.org/wp-content/uploads/20190529122826/bs11.png'); 
                $("#GFG_DOWN").text("src attribute changed");
            }); 
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/d58925d4707880484092e8cf98c110c3.png)
*   **点击按钮后:**
    ![](img/c0a9e57260264e76c70ab3fe519ffdd2.png)