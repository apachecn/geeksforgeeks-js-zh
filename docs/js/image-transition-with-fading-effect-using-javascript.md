# 使用 JavaScript 的带有渐变效果的图像过渡

> 原文:[https://www . geesforgeks . org/image-transition-with-fading-effect-use-JavaScript/](https://www.geeksforgeeks.org/image-transition-with-fading-effect-using-javascript/)

给定一些图像，任务是使用 Javascript 创建从一个图像到另一个图像的缓慢过渡。
**先决条件:**在本文中，我们将使用以下 JavaScript 方法。

*   [设置区间()方法](https://www.geeksforgeeks.org/java-script-settimeout-setinterval-method/)
*   [clearInterval()方法](https://www.geeksforgeeks.org/javascript-cleartimeout-clearinterval-method/)
*   [异步/等待](https://www.geeksforgeeks.org/async-await-function-in-javascript/)
*   [承诺](https://www.geeksforgeeks.org/javascript-promises/)

**方法:**给定一些图像，任务是在有规律的间隔后改变图像，使其具有褪色或溶解效果。要定期更改图像，请使用**设置间隔()**方法。将图像保持在彼此之上，并通过定期更改 z-index 将最上面的图像移动到底部。
使用**异步功能**使图像过渡具有渐变效果。在异步函数内部，使用另一种 **setInterval()** 方法慢慢降低最上面图像的不透明度，直到不透明度变为 0。这样做，最上面的图像会慢慢消失。一旦最上面的图像完全消失，将其移动到最底部的位置并存储新的顶部图像索引。

*   **Javascript 代码:**

## java 描述语言

```html
<script>
    startImageTransition();

    function startImageTransition() {

        // images stores list of all images of
        // class test. This is the list of images
        // that we are going to iterate
        var images = document.getElementsByClassName("test");

        // Set opacity of all images to 1
        for (var i = 0; i < images.length; ++i) {
            images[i].style.opacity = 1;
        }

        // Top stores the z-index of top most image
        var top = 1;

        // cur stores the index of the image currently
        // on top images list contain images in the
        // same order they appear in HTML code
        /* The tag with class test which appears last
           will appear on top of all the images thus,
           cur is set to last index of images list*/
        var cur = images.length - 1;

        // Call changeImage function every 3 second
        // changeImage function changes the image
        setInterval(changeImage, 3000);

        // Function to transitions from one image to other
        async function changeImage() {

            // Stores index of next image
            var nextImage = (1 + cur) % images.length;

            // First set the z-index of current image to top+1
            // then set the z-index of nextImage to top
            /* Doing this make sure that the image below
               the current image is nextImage*/
            // if this is not done then during transition
            // we might see some other image appearning
            // when we change opacity of the current image
            images[cur].style.zIndex = top + 1;
            images[nextImage].style.zIndex = top;

            // await is used to make sure
            // the program waits till transition()
            // is completed
            // before executing the next line of code
            await transition();

            // Now, the transition function is completed
            // thus, we can say that the opacity of the
            // current image is now 0

            // Set the z-index of current image to top
            images[cur].style.zIndex = top;

            // Set the z-index of nextImage to top+1
            images[nextImage].style.zIndex = top + 1;

            // Increment top
            top = top + 1;

            // Change opacity of current image back to 1
            // since zIndex of current is less than zIndex
            // of nextImage
            /* changing it's opacity back to 1 will not
               make the image appear again*/
            images[cur].style.opacity = 1;

            // Set cur to nextImage
            cur = nextImage;
        }

        /* This function changes the opacity of
        current image at regular intervals*/
        function transition() {
            return new Promise(function (resolve, reject) {

                // del is the value by which opacity is
                // decreased every interval
                var del = 0.01;

                // id stores ID of setInterval
                // this ID will be used later
                // to clear/stop setInterval
                // after we are done changing opacity
                var id = setInterval(changeOpacity, 10);

                // changeOpacity() decreasing opacity of
                // current image by del
                // when opacity reaches to 0, we stops/clears
                // the setInterval and resolve the function
                function changeOpacity() {
                    images[cur].style.opacity -= del;
                    if (images[cur].style.opacity <= 0) {
                        clearInterval(id);
                        resolve();
                    }
                }
            })
        }
    }
</script>
```

*   **完整代码:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <title>
        Change Image Dynamically when User Scrolls
    </title>

    <style>
        body {
            text-align: center;
        }

        h1 {
            color: green;
        }

        img {
            position: absolute;
            left: 400px;
        }
    </style>

</head>

<body>
    <h1>GeeksforGeeks</h1>
    <b>A Computer Science Portal for Geeks</b>
    <div id="scroll-image">
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200318142245/CSS8.png"
             class="test" />
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200318142309/php7.png"
             class="test" />
        <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20200318142254/html9.png"
             class="test" />
    </div>

    <script>
        startImageTransition();

        function startImageTransition() {
            var images = document.getElementsByClassName("test");

            for (var i = 0; i < images.length; ++i) {
                images[i].style.opacity = 1;
            }

            var top = 1;

            var cur = images.length - 1;

            setInterval(changeImage, 3000);

            async function changeImage() {

                var nextImage = (1 + cur) % images.length;

                images[cur].style.zIndex = top + 1;
                images[nextImage].style.zIndex = top;

                await transition();

                images[cur].style.zIndex = top;

                images[nextImage].style.zIndex = top + 1;

                top = top + 1;

                images[cur].style.opacity = 1;

                cur = nextImage;

            }

            function transition() {
                return new Promise(function(resolve, reject) {
                    var del = 0.01;

                    var id = setInterval(changeOpacity, 10);

                    function changeOpacity() {
                        images[cur].style.opacity -= del;
                        if (images[cur].style.opacity <= 0) {
                            clearInterval(id);
                            resolve();
                        }
                    }

                })
            }
        }
    </script>

</body>

</html>
```

*   **输出:**

![](img/83211308bc303b63f491afedf86813a6.png)

**注意:**图像变化的时间间隔应大于使图像不透明度小于或等于 0 所需的时间。