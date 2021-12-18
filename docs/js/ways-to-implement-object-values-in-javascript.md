# 在 JavaScript 中实现 Object.values()的方法

> 原文:[https://www . geesforgeks . org/实现方法-对象-值-in-javascript/](https://www.geeksforgeeks.org/ways-to-implement-object-values-in-javascript/)

有一个方法 **Object.values()** 返回 JavaScript Object 的值。在这里，我们将在 JavaScript 的帮助下看到这种方法的所有其他替代方法。这里讨论几个方法。

**方法 1:** 使用 [**Object.keys()方法**](https://www.geeksforgeeks.org/object-keys-javascript/) 获取密钥，然后使用 [**map()方法**](https://www.geeksforgeeks.org/javascript-array-map-method/) 将密钥映射到值并将值存储在数组中。

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Alternative version for Object.values() in JavaScript.
        </title>
    </head>

    <body style="text-align:center;">
        <h1 style="color: green">  
                GeeksForGeeks  
            </h1>
        <p id="GFG_UP">
        </p>
        <button onclick="gfg_Run()">
            Click Here
        </button>
        <p id="GFG_DOWN">
        </p>
        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var arr = [];
            var obj = {
                a: 'val_1',
                b: 'val_2'
            };
            el_up.innerHTML = 
              "Click on the button to get the values.<br>Object = "
            + JSON.stringify(obj);

            function gfg_Run() {
                var val = Object.keys(obj).map(function(e) {
                    return obj[e];
                });
                el_down.innerHTML = JSON.stringify(val);
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/913944867844adc7c89df7b08797ed7f.png)

**方法 2:** 通过运行循环来访问对象的每个属性，并且每次都将该值放入数组中。[使用**obj . hasown property()**T5】和](https://www.geeksforgeeks.org/javascript-hasownproperty-method/)[T7】push()方法 T9。](https://www.geeksforgeeks.org/javascript-array-prototype-push-function/)

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Alternative version for Object.values() in JavaScript.
        </title>
    </head>

    <body style="text-align:center;">
        <h1 style="color: green">  
                GeeksForGeeks  
            </h1>
        <p id="GFG_UP">
        </p>
        <button onclick="gfg_Run()">
            Click Here
        </button>
        <p id="GFG_DOWN">
        </p>
        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var arr = [];
            var obj = {
                a: 'val_1',
                b: 'val_2'
            };
            el_up.innerHTML = 
              "Click on the button to get the values.<br>Object = " 
            + JSON.stringify(obj);

            function getValues(obj) {
                var ret = [];
                for (var i in obj) {
                    if (obj.hasOwnProperty(i)) {
                        ret.push(obj[i]);
                    }
                }
                return ret;
            }

            function gfg_Run() {
                el_down.innerHTML = JSON.stringify(getValues(obj));
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/913944867844adc7c89df7b08797ed7f.png)

**方法 3:(ES6 格式)**使用 [**Object.keys()方法**](https://www.geeksforgeeks.org/object-keys-javascript/) 获取密钥，然后使用 [**map()方法**](https://www.geeksforgeeks.org/javascript-array-map-method/) 将密钥映射到值并将值存储在数组中。

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Alternative version for Object.values() in JavaScript.
        </title>
    </head>

    <body style="text-align:center;">
        <h1 style="color: green">  
                GeeksForGeeks  
            </h1>
        <p id="GFG_UP">
        </p>
        <button onclick="gfg_Run()">
            Click Here
        </button>
        <p id="GFG_DOWN">
        </p>
        <script>
            var el_up = document.getElementById("GFG_UP");
            var el_down = document.getElementById("GFG_DOWN");
            var arr = [];
            var obj = {
                a: 'val_1',
                b: 'val_2'
            };
            el_up.innerHTML = 
              "Click on the button to get the values.<br>Object = "
            + JSON.stringify(obj);

            function gfg_Run() {
                el_down.innerHTML = Object.keys(obj).map(e => obj[e]);
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/913944867844adc7c89df7b08797ed7f.png)