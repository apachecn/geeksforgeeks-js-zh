# 如何使用 JavaScript 将鼠标指针移动到特定位置？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将鼠标指针移动到特定位置/](https://www.geeksforgeeks.org/how-to-move-mouse-pointer-to-a-specific-position-using-javascript/)

在本文中，我们将学习如何使用 JavaScript 将鼠标指针移动到网络浏览器中的任何特定位置。在我们开始之前，您需要知道，使用 Javascript 将鼠标指针移动到某个位置实际上是不可能的，这样的功能我们很容易误用，但是我们可以模拟类似的东西。

在本文中，我们将学习如何将鼠标指针从一个指针移动到另一个指针。

*   由于我们不能使用 JavaScript 制作实际的鼠标指针，所以我们使用图像作为光标。
*   假设变量 x，y，px，py，x1，x2

    ```html
    x: x-position of the actual mouse pointer
    y: y-position of the actual mouse pointer
    x1: x-position where we want the mouse to appear
    x2: y-position where we want the mouse to appear

    Now, let
    x + px = x1
    px = x1 - x

    similarly,
    py = y1 - y

    Now, px, py is the relative position of x, y with respect to x1, y1.
    The position where our image cursor will appear with respect to x1, 
    y1 will be given by 
    x + px and y + py
    for all x, y
    ```

*   现在，问题是如何检测点击，因为鼠标光标可能不在指针上。为此，我们使用 document.elementFromPoint(x+px，y+py)，在其中传递图像光标的位置。这会给我们元素的对象，图像光标在上面。获得所需对象后，我们可以调用该对象。

**示例:**

*   **HTML 代码:**

    ```html
    <!DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="utf-8" />
    </head>

    <body>
        <img id="cursor" src=
    "https://media.geeksforgeeks.org/wp-content/uploads/20200319212118/cursor2.png"
            width="15" height="20" />

        <p>
            <button id="b1">BUTTON1</button>
        </p>

        <p>
            <button id="b2">BUTTON2</button>
        </p>

    </body>

    </html>                    
    ```

*   **CSS 代码:**t0]
*   **JavaScript 代码:**t0]

**最终解决方案:**在本节中，我们将把上述所有部分合并为一个部分，并执行任务。

```html
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="utf-8" />
    <title></title>
    <style>
        img {
            pointer-events: none;
            /* doing this makes sure .elementFromPoint 
               do not acquires the image cursor object */
            position: absolute;
        }
        /* makes the cursor invisible */

        * {
            cursor: none;
        }
    </style>
</head>

<body>
    <img id="cursor" src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200319212118/cursor2.png" 
         width="15" height="20" />

    <p>
        <button id="b1">BUTTON1</button>
    </p>

    <p>
        <button id="b2">BUTTON2</button>
    </p>

    <script>
        var x, y;
        var px, py;
        px = py = 0;

        // Image of cursor
        var cursor = document.getElementById("cursor"); 

        // Button 1
        var b1 = document.getElementById("b1");

        // Button 2
        var b2 = document.getElementById("b2");

        /* mutex is used to avoid multiple click event from
           firing at the same time due to different position
           of image cursor and actual cursor 
           Using mutex avoid any conflicts if original cursor and
           image cursor are both on a clickable element
           This makes sure only 1 click event is triggered at a time*/

        var mutex = false;

        /*
         The following event is selecting the element
         on the image cursor and fires click() on it.
         The following event is triggered only when mouse is pressed.
         */
        window.addEventListener("mouseup", function(e) {

            // gets the object on image cursor position
            var tmp = document.elementFromPoint(x + px, y + py); 
            mutex = true;
            tmp.click();
            cursor.style.left = (px + x) + "px";
            cursor.style.top = (py + y) + "px";
        })

        /* The following event listener moves the image pointer 
         with respect to the actual mouse cursor
         The function is triggered every time mouse is moved */
        window.addEventListener("mousemove", function(e) {

            // Gets the x,y position of the mouse cursor
            x = e.clientX;
            y = e.clientY;

            // sets the image cursor to new relative position
            cursor.style.left = (px + x) + "px";
            cursor.style.top = (py + y) + "px";

        });

        /* The following function re-calculates px,py 
           with respect to new position
           Clicking on b1 moves the pointer to b2
           Clicking on b2 moves the pointer to b1 */

        b1.onclick = function() {
            if (mutex) {
                mutex = false;
                px = b2.offsetLeft - x;
                py = b2.offsetTop - y;
            }
        }

        b2.onclick = function() {
            if (mutex) {
                mutex = false;
                px = b1.offsetLeft - x;
                py = b1.offsetTop - y;
            }
        }
    </script>

</body>

</html>
```

**输出:**
![](https://i.imgur.com/FR4ImPy.gif)