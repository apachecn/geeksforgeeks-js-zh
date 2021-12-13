# 如何在 JavaScript 中给`String`类添加方法？

> 原文:[https://www . geesforgeks . org/如何将方法添加到 javascript 中的字符串类/](https://www.geeksforgeeks.org/how-to-add-method-to-string-class-in-javascript/)

任务是在 JavaScript 中向 String 类添加一个方法。有两种方法用适当的例子描述:

**方法 1:** 使用 **Object.defineProperty()方法**，该方法用于直接为对象定义新属性，或者修改现有属性。它需要 3 个参数，第一个是对象，第二个是属性名，最后一个是属性描述。在本例中，返回字符串长度的总和。

*   **例:**

    ```html
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Add method to String class in JavaScript
        </title>

        <style>
            body {
                text-align: center;
            }

            h1 {
                color: green;
            }
        </style>
    </head>

    <body>
        <h1>GeeksforGeeks</h1>

        <p id="GFG_UP"></p>

        <button onClick="GFG_Fun()">
            click here
        </button>

        <p id="GFG_DOWN"></p>

        <script>
            var up = document.getElementById('GFG_UP');
            var down = document.getElementById('GFG_DOWN');

            var str1 = "GeeksforGeeks";
            var str2 = "A Computer Science Portal";

            up.innerHTML = "Click on button to get the "
                        + "sum of length of the both "
                        + "strings<br>Str1 - '" + str1
                        + "'<br>Str2 - '" + str2 + "'";

            Object.defineProperty(String.prototype,
            'SumOfLength', {
                value: function(param) {
                    return this.length + param.length;
                }
            });

            function GFG_Fun() {
                const res = str1.SumOfLength(str2);
                down.innerHTML = res;
            }
        </script>
    </body>

    </html>
    ```

*   **输出:** ![](img/7766618f3510ec6799907166d9a897b8.png)

**方法 2:** 使用**String . prototype . property name**向 String 类添加一个新方法。定义一个方法，该方法接受对象传递的参数并执行所需的操作。在本例中，返回字符串长度的总和。

*   **例:**

    ```html
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Add method to String
            class in JavaScript
        </title>

        <style>
            body {
                text-align: center;
            }

            h1 {
                color: green;
            }
        </style>
    </head>

    <body>
        <h1>GeeksforGeeks</h1>

        <p id="GFG_UP"></p>

        <button onClick="GFG_Fun()">
            click here
        </button>

        <p id="GFG_DOWN"></p>

        <script>
            var up = document.getElementById('GFG_UP');
            var down = document.getElementById('GFG_DOWN');

            var str1 = "GeeksforGeeks";
            var str2 = "A Computer Science Portal";

            up.innerHTML = "Click on button to get the "
                        + "sum of length of the both "
                        + "strings<br>Str1 - '" + str1
                        + "'<br>Str2 - '" + str2 + "'";

            String.prototype.SumOfLength = function( arg ) {
                return this.length + arg.length;
            };
            function GFG_Fun() {
                const res = str1.SumOfLength(str2);
                down.innerHTML = res;
            }
        </script>
    </body>

    </html>
    ```

*   **输出:** ![](img/7766618f3510ec6799907166d9a897b8.png)