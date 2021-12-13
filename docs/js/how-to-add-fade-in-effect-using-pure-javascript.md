# 如何用纯 JavaScript 添加淡入效果？

> 原文:[https://www . geesforgeks . org/如何使用纯 javascript 添加淡入效果/](https://www.geeksforgeeks.org/how-to-add-fade-in-effect-using-pure-javascript/)

淡入淡出效果被描述为所选部分不透明度的逐渐增加和减少。换句话说，褪色效应被称为不透明度随时间的增加和减少。当这种效果随着不透明度的逐渐增加而应用时，它被称为淡入效果。这是用于以选定的时间间隔在页面上的选定部分应用淡入的效果。淡出和淡入效果在网页项目中使用非常好，因为它强调网页的样式。我们在这些逻辑中使用 **[【设置区间】()法](https://www.geeksforgeeks.org/java-script-settimeout-setinterval-method/)** 和 **[clearInterval()法](https://www.geeksforgeeks.org/javascript-cleartimeout-clearinterval-method/)** 。下面我们将通过适当的描述和例子来介绍两种方法。

**[使用 setInterval()方法:](https://www.geeksforgeeks.org/java-script-settimeout-setinterval-method/)** 在页面加载时，我们正在调用一个名为 **[fadeIn()方法](https://www.geeksforgeeks.org/jquery-fadein-method/)** 的函数。其中我们使用的是 **setInterval()方法**，它取两个参数一个是函数引用(本例中是 show()，另一个是 timer(以数字表示)，在每个给定的时间间隔后都会调用 **[show()函数](https://www.geeksforgeeks.org/jquery-effect-show-method/)** 。在 **show()函数**中，我们在名为“不透明度”的变量中获取属性不透明度，并在每次调用 **fadeIn()函数**时将其增加 0.1。最初，选定部分的不透明度设置为 0。两个变量不透明度和**有效间隔**在脚本标签中声明。可变不透明度处理项目的不透明度，而 **intervalID** 用于调用 **clearInterval()函数**。然后 **window.onload=fadeIn** ，用于自动调用 **fadeIn()功能**。 **fadeIn()函数**调用内置方法 setInterval()，该方法取两个参数，一个是函数引用(本例中为 show()，另一个是时间间隔(取所选间隔后的函数引用)。在 setInterval()中，每隔 200 毫秒调用 show()函数，在这 200 毫秒中，我们检查主体的不透明度(变量主体在 id 的帮助下保持完整的主体)，如果它小于 1，不透明度将增加 0.1，否则将调用 **clearInterval()函数**，这将停止对 **show()** 的函数调用。

**注意:**将所选部分的不透明度设置为零，以了解效果。

*   **例:**

    ```html
    <!DOCTYPE html>
    <html>

    <head>
        <title>
          fade-in effect on page load using JavaScript
        </title>
        <script type="text/javascript">
            var opacity = 0;
            var intervalID = 0;
            window.onload = fadeIn;

            function fadeIn() {
                setInterval(show, 200);
            }

            function show() {
                var body = document.getElementById("body");
                opacity = Number(window.getComputedStyle(body)
                                 .getPropertyValue("opacity"));
                if (opacity < 1) {
                    opacity = opacity + 0.1;
                    body.style.opacity = opacity
                } else {
                    clearInterval(intervalID);
                }
            }
        </script>
    </head>

    <body id="body" style="opacity: 0;">
        <br>
        <h1 style="color: green">GeeksforGeeks</h1>
        <b> 
          How to create fade-in effect 
          on page load using javascript 
        </b>
        <p>
          This page will fade-in after loading
        </p>
    </body>
    <html>
    ```

*   **输出:** ![](img/57e4dd3c3e9b7600396b94a04c74b606.png)

**[使用 clearInterval()方法:](https://www.geeksforgeeks.org/javascript-cleartimeout-clearinterval-method/)** 在这种方法中，完整的逻辑被写在一个变量里面，这个变量是在 setInterval()方法的帮助下完成的，这里完整的函数将被写在函数引用的地方。这种方法相对容易理解。不透明度的默认值为 1。所以我们必须把它设为零。观察输出 **window.onload=fadeIn** ，用于自动调用 fadeIn()功能。现在在 fadeIn()函数中声明 3 个变量:

*   **淡入淡出:**是提取要应用淡入效果的部分。
*   **不透明度:**是处理提取部分的不透明度。
*   **intervalID:** 是处理完整逻辑和终止逻辑。

现在不是写函数引用，而是要写一个完整的函数，每隔 200 毫秒就会反复调用一次，增加不透明度。现在在书面函数中，每次调用时，提取部分的不透明度与 1 进行比较

*   如果发现不透明度小于 1，不透明度将增加 0.1，并应用于提取的部分。
*   如果发现不透明度为 1 或大于 1，调用 clearInterval()函数终止函数函数调用。

*   **例:**

    ```html
    <!DOCTYPE html>
    <html>

    <head>
        <title>
          fade-in effect on page load using JavaScript
        </title>
        <script type="text/javascript">
            window.onload = fadeIn;

            function fadeIn() {
                var fade = document.getElementById("body");
                var opacity = 0;
                var intervalID = setInterval(function() {

                    if (opacity < 1) {
                        opacity = opacity + 0.1
                        fade.style.opacity = opacity;
                    } else {
                        clearInterval(intervalID);
                    }
                }, 200);
            }
        </script>

    </head>

    <body id="body" style="opacity:0;">
        <br>
        <h1 style="color: green">GeeksforGeeks</h1>
        <b> 
          How to create fade-in effect 
          on page load using javascript 
        </b>
        <p>
          This page will fade-in after loading
        </p>
    </body>

    </html>
    ```

*   **输出:**这个输出视频在循环中，这就是为什么它在获得不透明度 1 后没有停止。它会一次又一次地自动加载。
    T3】

**注意:**如果增量值大于 0.1，则淡入更快。如果时间间隔缩短，则淡入也更快。