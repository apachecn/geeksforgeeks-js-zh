# 如何用 JavaScript 改变视频播放速度？

> 原文:[https://www . geesforgeks . org/how-change-video-playing-speed-use-JavaScript/](https://www.geeksforgeeks.org/how-to-change-video-playing-speed-using-javascript/)

在本文中，我们将看到如何使用 [HTML5 视频标签](https://www.geeksforgeeks.org/html5-video/)来更改嵌入在 HTML 文档中的视频的*播放速度*。

我们可以使用 *playbackRate* 属性设置新的播放速度。它有以下语法。

**语法:**

```html
let video = document.querySelector('video')
video.playbackRate = newPlaybackRate
```

我们也可以使用 *defaultPlaybackRate* 属性设置默认播放速度。它有以下语法。

**语法:**

```html
 let video = document.querySelector('video')
 video.defaultPlaybackRate = 4
 video.load()
```

**示例:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">

    <style>
        body {
            text-align: center;
            margin-top: 2%;
        }

        h1 {
            color: green;
        }

        p {
            margin-top: 2%;
        }

        button {
            margin-right: 20px;
        }
    </style>
</head>

<body>
    <h1>GeeksforGeeks</h1>

    <video width="890" height="500" controls loop>
        <source src="sample.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <p>
        <button onclick="increase()">Increase Speed</button>
        <button onclick="decrease()">Decrease Speed</button>
    </p>

    <script>
        let video = document.querySelector('video');

        // Set the default playing speed
        video.defaultPlaybackRate = 0.5

        // Loading the video after setting 
        video.load();

        function increase() {

            // Increasing the playing speed by 1
            video.playbackRate += 1;
        }

        function decrease() {

            // Decreasing the playing speed by 1
            if (video.playbackRate > 1)
                video.playbackRate -= 1;
        }
    </script>
</body>

</html>
```

**输出:**

![](img/f3d03739ee43ca6a19923c9c6bbf7acb.png)