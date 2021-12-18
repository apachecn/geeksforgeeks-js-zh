# 如何使用 JavaScript / jQuery 禁用 HTML 链接？

> 原文:[https://www . geesforgeks . org/如何禁用-html-link-使用-javascript-jquery/](https://www.geeksforgeeks.org/how-to-disable-html-links-using-javascript-jquery/)

给定一个 HTML 链接，任务是使用 JavaScript/jQuery 禁用该链接。

**使用 JavaScript 禁用 HTML 链接**

*   **createAttribute() Method:** This method creates an attribute with the defined name and returns the attribute as an attribute object.

    **语法:**

    ```
    document.createAttribute(attrName)
    ```

    **参数:**该方法接受单参数**属性**，该属性为必选项。它指定创建的属性的名称。

    **返回值:**返回节点对象，表示创建的属性。

*   **setAttribute() Method:** This method adds the defined attribute to an element and gives it to the passed value. In case of the specified attribute already exists, the value is set/changed.

    **语法:**

    ```
    element.setAttribute(attrName, attrValue)
    ```

    **参数:**

    *   **attrName:** 此参数为必选项。它指定要添加的属性的名称。
    *   **属性值:**此参数为必填项。它指定要添加的属性值。
*   **setAttributeNode() Method:** This method adds the specified attribute node to an element. In case of the specified attribute already exists, this method replaces it.

    **语法:**

    ```
    element.setAttributeNode(attributeNode)
    ```

    **参数:**该方法接受单参数**属性节点**，这是必需的。它指定要添加的属性节点。

**示例 1:** 本示例在 **setAttribute()方法**的帮助下，将禁用的类添加到< a >元素中。

```
<!DOCTYPE HTML>  
<html>  
    <head> 
        <title> 
            How to disable HTML links
            using JavaScript
        </title>

        <style>
            a.disabled {
                pointer-events: none;
            }
        </style>
    </head> 

    <body style = "text-align:center;">  

        <h1 style = "color:green;" >  
            GeeksForGeeks  
        </h1>

        <a href = "#" id = "GFG_UP">
            LINK
        </a>

        <br><br>

        <button onclick = "gfg_Run()"> 
            disable
        </button>

        <p id = "GFG_DOWN" style =
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            var link = document.getElementById('GFG_UP');
            var down = document.getElementById('GFG_DOWN');

            function gfg_Run() {
              link.setAttribute("class", "disabled");
              link.setAttribute("style", "color: black;");
              down.innerHTML = "Link disabled";
            }         
        </script> 
    </body>  
</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/f09f01438a1fe121f523a624b8ab961e.png)
*   **点击按钮后:**
    ![](img/52837db223e91d051a2e243e912f1b81.png)

**示例 2:** 本示例在 **setAttributeNode()方法**的帮助下，通过首先使用 **createAttribute()方法**创建一个属性，然后将其添加到 **< a >** 元素中，将类 disable 添加到< a >元素中。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            How to disable HTML links
            using JavaScript
        </title>

        <style>
            a.disabled {
                pointer-events: none;
            }
        </style>
    </head> 

    <body style = "text-align:center;"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <a href = "#" id = "GFG_UP">
            LINK
        </a>

        <br><br>

        <button onclick = "gfg_Run()"> 
            disable
        </button>

        <p id = "GFG_DOWN" style =
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            var link = document.getElementById('GFG_UP');
            var down = document.getElementById('GFG_DOWN');

            function gfg_Run() {
                var attr = document.createAttribute("class");
                attr.value = "disabled";                         
                link.setAttributeNode(attr);
                link.setAttribute("style", "color: black;");
                down.innerHTML = "Link disabled";
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/f09f01438a1fe121f523a624b8ab961e.png)
*   **点击按钮后:**
    ![](img/52837db223e91d051a2e243e912f1b81.png)

**使用 jQuery 禁用 HTML 链接**

*   **jQuery prop() Method:** This method set/return properties and values of the matched elements. If this method is used to return the property value, it returns the value of the first selected element. If this method is used to set property values, it sets one or more property/value pairs for the set of selected elements.

    **语法:**

    *   **返回房产价值:**

        ```
        $(selector).prop(property)

        ```

    *   **设置属性和值:**

        ```
        $(selector).prop(property,value)

        ```

    *   **使用函数设置属性和值:**

        ```
        $(selector).prop(property,function(index,currentvalue))

        ```

    *   **设置多个属性和值:**

        ```
        $(selector).prop({property:value, property:value,...})

        ```

    **参数:**

    *   **属性:**此参数指定属性的名称。
    *   **值:**此参数指定属性的值。
    *   **函数(索引，currentvalue):** 此参数指定一个返回要设置的属性值的函数。
        *   **索引:**该参数接收集合中元素的索引位置。
        *   **当前值:**此参数接收选定元素的当前属性值。
*   **addClass() Method:** This method adds one or more than one class names to the specified elements. This method does not do anything with existing class attributes, it adds one or more than one class names to the class attribute.

    **语法:**

    ```
    $(selector).addClass(className,function(index,currentClass))

    ```

    **参数:**

    *   **类名:**此参数为必选项。它指定一个或多个要添加的类名。
    *   **函数(索引，currentClass):** 此参数可选。它指定一个函数，该函数返回一个或多个要添加的类名。
        *   **索引:**返回元素在集合中的索引位置。
        *   **类名:**返回所选元素的当前类名。

**示例 1:** 本示例在 **addClass()方法**的帮助下，将类(“禁用”)添加到< a >元素中。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            How to disable HTML links
            using jQuery
        </title>

        <script src =
"https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js">
        </script>

        <style>
            a.disabled {
                pointer-events: none;
            }
        </style>
    </head> 

    <body style = "text-align:center;"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <a href = "#" id = "GFG_UP">
            LINK
        </a>

        <br><br>

        <button onclick = "gfg_Run()"> 
            disable
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            function gfg_Run() {
                $('a').addClass("disabled");
                $('a').css('color', 'black');
                $('#GFG_DOWN').text("Link disabled");
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/f09f01438a1fe121f523a624b8ab961e.png)
*   **点击按钮后:**
    ![](img/52837db223e91d051a2e243e912f1b81.png)

**示例 2:** 本示例在 **prop()方法**的帮助下，将类(“禁用”)添加到< a >元素中。

```
<!DOCTYPE HTML> 
<html> 
    <head> 
        <title> 
            How to disable HTML links
            using jQuery
        </title>

        <script src = 
"https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js">
        </script>

        <style>
            a.disabled {
                pointer-events: none;
            }
        </style>
    </head> 

    <body style = "text-align:center;"> 

        <h1 style = "color:green;" > 
            GeeksForGeeks 
        </h1>

        <a href = "#" id = "GFG_UP">
            LINK
        </a>

        <br><br>

        <button onclick = "gfg_Run()"> 
            disable
        </button>

        <p id = "GFG_DOWN" style = 
            "color:green; font-size: 20px; font-weight: bold;">
        </p>

        <script>
            function gfg_Run() {
                $('a').prop("class","disabled");
                $('a').css('color', 'black');
                $('#GFG_DOWN').text("Link disabled");
            }         
        </script> 
    </body> 
</html>                    
```

**输出:**

*   **点击按钮前:**
    ![](img/f09f01438a1fe121f523a624b8ab961e.png)
*   **点击按钮后:**
    ![](img/52837db223e91d051a2e243e912f1b81.png)