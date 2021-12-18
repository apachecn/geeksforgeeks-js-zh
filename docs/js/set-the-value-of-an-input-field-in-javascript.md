# 在 JavaScript 中设置输入字段的值

> 原文:[https://www . geeksforgeeks . org/set-JavaScript 中输入字段的值/](https://www.geeksforgeeks.org/set-the-value-of-an-input-field-in-javascript/)

有时我们需要设置<input>元素的默认值，这个例子解释了这样做的方法。

*   **文本值属性**
    该属性设置/返回文本字段的值属性的值。
    value 属性包含默认值、用户键入的值或脚本设置的值。
    **语法:**
    *   **返回价值属性:**

        ```
        textObject.value

        ```

    *   **设置值属性:**

```
textObject.value = text

```

**属性值:**

*   **文本:**指定输入文本字段的值。
*   **属性值:**此参数为必填项。它指定要添加的属性值。

*   **setAttribute method**
    This method adds the specified attribute to an element, and set it’s specified value.
    If the attribute already present, then it’s value is set/changed.
    **Syntax:**

    ```
    element.setAttribute(attributeName, attributeValue)

    ```

    **参数:**

    *   **属性名称:**此参数为必填项。它指定要添加的属性的名称。
    *   **属性值:**此参数为必填项。它指定要添加的属性值。

    **示例-1:** 本示例通过**文本值**属性将输入元素的值设置为**“文本值”**。

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <title>
            JavaScript 
          | Set the value of an input field.
        </title>
    </head>

    <body style="text-align:center;" id="body">
        <h1 style="color:green;">  
                GeeksForGeeks  
            </h1>
        <input type='text' id='id1' />
        <br>
        <br>
        <button onclick="gfg_Run()">
            click to set
        </button>
        <p id="GFG_DOWN" style="color:green; 
                                font-size: 20px;
                                font-weight: bold;">
        </p>
        <script>
            var el_down = document.getElementById("GFG_DOWN");
            var inputF = document.getElementById("id1");

            function gfg_Run() {
                inputF.value = "textValue";
                el_down.innerHTML = 
                       "Value = " + "'" + inputF.value + "'";
            }
        </script>
    </body>

    </html>
    ```

    **输出:**

    *   **点击按钮前:**
        ![](img/50029ee755189ae131319c67428cf2d7.png)
    *   **点击按钮后:**
        ![](img/dc743444d34697656cd88816a36c76ca.png)

    **示例-2:** 本示例通过**设置属性**方法将输入元素的值设置为**“默认值”**。

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <title>
            JavaScript 
          | Set the value of an input field.
        </title>
    </head>

    <body style="text-align:center;" id="body">
        <h1 style="color:green;">  
                GeeksForGeeks  
            </h1>
        <input type='text' id='id1' />
        <br>
        <br>
        <button onclick="gfg_Run()">
            click to set
        </button>
        <p id="GFG_DOWN" style="color:green; 
                                font-size: 20px;
                                font-weight: bold;">
        </p>
        <script>
            var el_down = document.getElementById("GFG_DOWN");
            var inputF = document.getElementById("id1");

            function gfg_Run() {
                inputF.setAttribute('value', 'defaultValue');
                el_down.innerHTML = 
                       "Value = " + "'" + inputF.value + "'";
            }
        </script>
    </body>

    </html>
    ```

    **输出:**

    *   **点击按钮前:**
        ![](img/50029ee755189ae131319c67428cf2d7.png)
    *   **点击按钮后:**
        ![](img/e45390f55e88c7c2cca0d99749618673.png)

    JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。