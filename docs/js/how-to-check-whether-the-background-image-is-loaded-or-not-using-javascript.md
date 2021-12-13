# 如何用 JavaScript 检查背景图片是否加载？

> 原文:[https://www . geeksforgeeks . org/如何检查后台图像是否使用 javascript 加载/](https://www.geeksforgeeks.org/how-to-check-whether-the-background-image-is-loaded-or-not-using-javascript/)

在 JavaScript 中， **onload** 事件用于检查窗口是否加载。同样，我们可以使用该事件来检查特定元素是否已经加载。有两种方法可以检查背景图像是否已加载。

**语法:**

*   使用超文本标记语言:

    ```html
    <element onload="myScript">
    ```

*   在 JavaScript 中使用 *onload* 属性:

    ```html
    object.onload = function(){myScript};

    ```

*   在 JavaScript 中使用 **addEventListener()** 方法

    ```html
    object.addEventListener("load", myScript);
    ```

**HTML 方式:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js">
    </script>

    <style>
        #bg_img {
            width: 50vw;
            height: 50vh;
        }
    </style>
</head>

<body>
    <h2>Welcome To GFG</h2>

    <p>
        Default code has been 
        loaded into the Editor.
    </p>

    <img id="bg_img" onload="loadImage()" />

    <p id="img_status"></p>

    <script>
        function loadImage() {
            document.getElementById("img_status")
                    .innerHTML = "image loaded";
        }
        document.getElementById("bg_img").src =
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png";

        let ele = document.getElementById("bg_img");
    </script>
</body>

</html>
```

**输出:**

![](img/7ed4b38d1defe26bce2a26e3981d098c.png)

**使用*加载*属性:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js">
    </script>

    <style>
        #bg_img {
            width: 50vw;
            height: 50vh;
        }
    </style>
</head>

<body>
    <h2>Welcome To GFG</h2>

    <p>
        Default code has been 
        loaded into the Editor.
    </p>

    <img id="bg_img" />

    <p id="img_status"></p>

    <script>
        let ele = document.getElementById("bg_img");
        ele.onload = (e) => {
            document.getElementById("img_status")
                    .innerHTML = "image loaded";
        };
        ele.src = 
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png";
    </script>
</body>

</html>
```

**输出:**

![](img/7ed4b38d1defe26bce2a26e3981d098c.png)

**使用 addEventListener()方法:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <style>
        #bg_img {
            width: 50vw;
            height: 50vh;
        }
    </style>
</head>

<body>
    <h2>Welcome To GFG</h2>

    <p>
        Default code has been 
        loaded into the editor
    </p>

    <img id="bg_img" />

    <p id="img_status"></p>

    <script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js">
    </script>

    <script>
        let ele = document.getElementById("bg_img");
        ele.addEventListener("load", (e) => {
            document.getElementById("img_status")
                    .innerHTML = "image loaded";
        });

        ele.src =
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png";
    </script>
</body>

</html>
```

**输出:**

![](img/7ed4b38d1defe26bce2a26e3981d098c.png)

**注意:**要使用 jQuery，请用以下内容替换事件侦听器代码–

```html
$("#bg_img").on("load", function () {
  window.alert("Image has loaded", 1);
});

```