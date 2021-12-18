# 如何在 JavaScript 中发出哔哔声？

> 原文:[https://www . geesforgeks . org/如何用 javascript 发出哔哔声/](https://www.geeksforgeeks.org/how-to-make-a-beep-sound-in-javascript/)

网站中的蜂鸣声可用于以下任务:

*   警报通知
*   让网站更具互动性

这些声音可以有更多的用例。这完全取决于一个人的创造力和需求。通常，我们用 Javascript 创建一个函数，并在需要时调用该函数。在本教程中，我们使用一个按钮，使用 **onclick** 方法播放“哔”声。

**方法一:**使用 Javascript 中的**音频**功能加载音频文件。

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" 
        content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <h1>Press the Button</h1>

    <button onclick="play()">Press Here!</button>

    <script>
        function play() {
            var audio = new Audio(
'https://media.geeksforgeeks.org/wp-content/uploads/20190531135120/beep.mp3');
            audio.play();
        }
    </script>
</body>
</html>
```

**输出:**
![](img/bf2e5b8918738e8400c1201f7c9028ba.png)

**方法二:**使用 html 中的 **[音频](https://www.geeksforgeeks.org/html-dom-audio-object/)** 标签，用 Javascript 播放。

```
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" 
        content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <h1>Press the Button</h1>

    <audio id="chatAudio" >
        <source src=
"https://media.geeksforgeeks.org/wp-content/uploads/20190531135120/beep.mp3" 
        type="audio/mpeg">
    </audio>
    <button onclick="play()">Press Here!</button>

    <script>
        var audio = document.getElementById('chatAudio');
        function play(){
            audio.play()
        }
    </script>
</body>
</html>
```

**输出:**
![](img/bf2e5b8918738e8400c1201f7c9028ba.png)