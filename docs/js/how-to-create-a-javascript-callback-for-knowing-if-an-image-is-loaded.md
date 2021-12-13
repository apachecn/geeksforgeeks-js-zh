# 如何创建一个 JavaScript 回调来知道是否加载了图像？

> 原文:[https://www . geesforgeks . org/如何创建 javascript 回调以了解是否加载了图像/](https://www.geeksforgeeks.org/how-to-create-a-javascript-callback-for-knowing-if-an-image-is-loaded/)

任务是了解图像是否是使用 JavaScript 回调方法加载的。请参考 [JavaScript 回调。](https://www.geeksforgeeks.org/javascript-callbacks/)

**方法 1:** 使用*。完成*属性。

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <title>
        Create a JavaScript callback for
        knowing if an image is loaded
    </title>

    <style>
        #sologo {
            height: 100%;
            width: 100%;
        }
    </style>
</head>

<body>

    <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png"
        alt="Loading Image" id="sologo" />

    <script type="text/javascript">
        let img = document.querySelector('img')

        function loaded() {
            alert('loaded')
        }

        if (img.complete) {
            loaded()
        } else {
            img.addEventListener('load', loaded)
            img.addEventListener('error', function () {
                alert('error')
            })
        }
    </script>
</body>

</html>
```

**Output:**
![](img/9386a9ec7aa6a61fe5a43f4a44556ac8.png)

**注意:**该程序将持续检查图像是否使用*加载。完成 *img* 元素的*属性。它还会检查错误。当图像被加载时，它将通过“已加载”警告消息框发出警告。

**方法二:**使用 *image.onload()* 方法

## 超文本标记语言

```html
<!DOCTYPE html>
<html>

<head>
    <title>
        Create a JavaScript callback for
        knowing if an image is loaded
    </title>

    <style>
        #sologo {
            height: 100%;
            width: 100%;
        }
    </style>
</head>

<body>
    <img src="#" alt="Loading Image" id="sologo" />

    <script type="text/javascript">
        window.onload = function () {

            let logo = document.getElementById('sologo');

            logo.onload = function () {
                alert("loaded");
            };

            setTimeout(function () {
                logo.src = 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png';
            }, 5000);
        };
    </script>
</body>

</html>
```

**Output:**
![](img/9386a9ec7aa6a61fe5a43f4a44556ac8.png)

**注意:**在该方法中， *Image.onload()* 正在持续检查图像是否加载。如果图像在 5 秒内没有加载，它将超时并显示一个错误。如果在某个设定时间后加载了图像，它会发出警告消息，提示“图像已加载”。