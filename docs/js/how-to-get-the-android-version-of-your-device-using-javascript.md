# 如何使用 JavaScript 获取设备的安卓版本？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 获取设备的安卓版本/](https://www.geeksforgeeks.org/how-to-get-the-android-version-of-your-device-using-javascript/)

任务是在 JavaScript 的帮助下检测用户的安卓版本。

这里讨论了两种方法，第一个例子使用 **[正则表达式](https://www.geeksforgeeks.org/javascript-regular-expressions/)** ，第二个例子使用 **[indexOf](https://www.geeksforgeeks.org/javascript-string-prototype-indexof-function/)** 方法搜索关键字**【安卓】**。

**注意:**这两个代码只有在安卓设备上运行时才会起作用。
**方法 1:** 在这种方法中，我们将使用 **[navigator.useragent 属性](https://www.geeksforgeeks.org/html-navigator-useragent-property/)** ，该属性返回浏览器发送给服务器的用户代理头的值。它包含关于浏览器的名称、版本和平台的信息。然后我们需要在返回的字符串中搜索关键字**‘安卓’**，并获取 temp 数组(包含版本)中的值，为此我们将使用一个 **[RegExp](https://www.geeksforgeeks.org/javascript-regular-expressions/)** 。如果 temp 不为 null，那么索引 0 处的值就是未定义的答案。

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Get the Android version of your device.
        </title>
        <script src=
    "https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js">
        </script>
        <style>
            body {
                text-align: center;
            }

            h1 {
                color: green;
            }

            .gfg {
                font-size: 20px;
                font-weight: bold;
            }

            #geeks {
                font-size: 24px;
                font-weight: bold;
                color: green;
            }
        </style>
    </head>

    <body>
        <h1> 
          GeeksForGeeks 
        </h1>
        <p class="gfg">
          Click on the button to get the android 
          version of the user.
        </p>
        <button onclick="GFG_Fun()">
            click here
        </button>
        <p id="geeks">
        </p>
        <script>
            var element = document.getElementById("body");

            function androidV(ua) {
                ua = (ua || navigator.userAgent).toLowerCase(); 
                var match = ua.match(/android\s([0-9\.]*)/i);
                return match ? match[1] : undefined;
            };
            function GFG_Fun() {            
                $('#geeks').html(androidV());
            }
        </script>
    </body>

    </html>                    
    ```

*   **输出:**
    ![](img/f84cf0832c521e0e50175ecc03a04d0b.png)

**方法 2** 在这种方法中，我们将使用 **[navigator.useragent 属性](https://www.geeksforgeeks.org/html-navigator-useragent-property/)** ，该属性返回浏览器发送给服务器的用户代理头的值。它包含关于浏览器的名称、版本和平台的信息。我们需要搜索的是字符串中是否有“安卓”关键词，为此我们将使用 **[的](https://www.geeksforgeeks.org/javascript-string-prototype-indexof-function/)** 索引。如果存在，则使用 **[获取关键字“安卓”之后的版本。slice()](https://www.geeksforgeeks.org/javascript-string-slice/)** 和 **[indexOf](https://www.geeksforgeeks.org/javascript-string-prototype-indexof-function/)** 。

*   **示例:**该示例实现了上述方法。

    ```
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            Get the Android version of your device.
        </title>
        <script src=
    "https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js">
        </script>
        <style>
            body {
                text-align: center;
            }

            h1 {
                color: green;
            }

            .gfg {
                font-size: 20px;
                font-weight: bold;
            }

            #geeks {
                font-size: 24px;
                font-weight: bold;
                color: green;
            }
        </style>
    </head>

    <body>
        <h1> 
          GeeksForGeeks 
        </h1>
        <p class="gfg">
          Click on the button to get the android 
          version of the user.
        </p>
        <button onclick="GFG_Fun()">
            click here
        </button>
        <p id="geeks">
        </p>
        <script>
            var element = document.getElementById("body");

            function GFG_Fun() {
                var androidV = null;
                var ua = navigator.userAgent;
                if (ua.indexOf("Android") >= 0) {
                    androidV = parseFloat(ua.slice(ua.indexOf("Android") + 8));
                }
                $('#geeks').html(androidV);
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/f84cf0832c521e0e50175ecc03a04d0b.png)