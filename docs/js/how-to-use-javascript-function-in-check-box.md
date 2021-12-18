# 如何在复选框中使用 javascript 函数？

> 原文:[https://www . geeksforgeeks . org/how-用法-JavaScript-函数 in-check-box/](https://www.geeksforgeeks.org/how-to-use-javascript-function-in-check-box/)

**复选框**用于用户可能希望在表单中选择多个选项的情况，例如“检查所有适用的”问题。选中了 HTML 复选框。通过将选中的属性设置为“是”值，复选框元素可以以预先选中的方式放置在网页上。

*   典型的形状为正方形。
*   允许用户通过单击选择选项。
*   期权共用一个名称。
*   Checkbox allow you to select more than ine options per group

    **示例:**在本例中，我们将使用基本 HTML 创建一个复选框和一个输入字段。当用户选中复选框时，输入字段将被激活。在第一部分，我们将使用 HTML 来创建基本结构，然后在第二部分，我们将使用 JavaScript 来完成剩下的功能任务。

    *   **超文本标记语言代码:**超文本标记语言文档，采用专用的超文本标记语言标签包装 JavaScript 代码。标签可以放在你的 HTML 的部分，在部分中，或者在结束标签之后，这取决于你希望 JavaScript 什么时候加载。

        ```
        <!DOCTYPE html>
        <html lang="en">
            <head>
                <meta charset="UTF-8" />
                <meta name="viewport"
                        content="width=device-width, initial-scale=1.0" />
                <link rel="stylesheet" href=
        "https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" />
            </head>
            <body>
                <div class="container">
                    <div class="row">
                        <div class="col-md-3"></div>
                        <div class="col-md-6">
                            <form>
                                <fieldset>
                                    <legend>
                                        <bold>Checkbox</bold>
                                    </legend>
                                    <div class="form-group">
                                        <label for="yesgraduated">
                                            Are you graduated?
                                        </label>
                                        <input id="yesgraduated"
                                           name="yesgraduated"
                                           type="checkbox" value="yes"
                                         onchange="graduatedFunction()" /> 
                                    <br />
                                    </div>
                                    <div id="graduated"
                                        class="form-group">
                                        <label for="degreename">
                                            Degree Name:
                                        </label>
                                        <input type="text"
                                            class="form-control"
                                            name="degreename"
                                            id="degreename" />
                                        <br />
                                    </div>
                                    <button type="button"
                                            class="btn btn-primary"
                                            value="Verify">
                                        Submit
                                    </button>
                                </fieldset>
                            </form>
                        </div>
                        <div class="col-md-3"></div>
                    </div>
                </div>
            </body>
        </html>                    
        ```

    *   **JavaScript 代码:**现在，在 JavaScript 代码中，我们试图给出在表单中包含学位的选项。用户需要知道他/她是否毕业。因此，当我们点击这个复选框，一个新的输入字段打开。因此，如果有人点击或不点击它，“渐变功能”功能将显示隐藏部分或不显示。

        ```
        <script>
            function graduatedFunction() {
                if (document.getElementById("yesgraduated")
                .checked) 
                {
                    document.getElementById("graduated")
                    .style.display = "inline";
                    document.getElementById("degreename")
                    .setAttribute("required", true);
                } else {
                    document.getElementById("degreename")
                    .removeAttribute("required");
                    document.getElementById("graduated")
                    .style.display = "none";
                }
            }
        </script>
        ```

    **完整代码:**是以上两个代码段的组合。

    ```
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="UTF-8" />
            <meta name="viewport"
                    content="width=device-width, initial-scale=1.0" />
            <link rel="stylesheet" href=
    "https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" />
            <script>
                function graduatedFunction() {
                    if (document.getElementById("yesgraduated")
                    .checked) 
                    {
                        document.getElementById("graduated")
                        .style.display = "inline";
                        document.getElementById("degreename")
                        .setAttribute("required", true);
                    } else {
                        document.getElementById("degreename")
                        .removeAttribute("required");
                        document.getElementById("graduated")
                        .style.display = "none";
                    }
                }
            </script>
        </head>
        <body>
            <div class="container">
                <div class="row">
                    <div class="col-md-3"></div>
                    <div class="col-md-6">
                        <form>
                            <fieldset>
                                <legend>
                                    <bold>Checkbox</bold>
                                </legend>
                                <div class="form-group">
                                    <label for="yesgraduated">
                                        Are you graduated?
                                    </label>
                                    <input id="yesgraduated"
                                           name="yesgraduated"
                                           type="checkbox" value="yes"
                                           onchange="graduatedFunction()" /> 
                                <br />
                                </div>
                                <div id="graduated" 
                                     class="form-group">
                                    <label for="degreename">
                                        Degree Name:
                                    </label>
                                    <input type="text" 
                                           class="form-control"
                                           name="degreename" 
                                           id="degreename" />
                                    <br />
                                </div>
                                <button type="button"
                                        class="btn btn-primary"
                                        value="Verify">
                                    Submit
                                </button>
                            </fieldset>
                        </form>
                    </div>
                    <div class="col-md-3"></div>
                </div>
            </div>
        </body>
    </html>                    
    ```

    **输出:**
    ![](img/4af3ddd843b7c94b46057099bf99b938.png)