# 如何使用 JavaScript 将语音转换为文本？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将语音转换为文本/](https://www.geeksforgeeks.org/how-to-convert-speech-into-text-using-javascript/)

在本文中，我们将学习使用 HTML 和 JavaScript 将语音转换为文本。

**方法:**我们添加了一个内容可编辑的“div”，通过它我们可以编辑任何 HTML 元素。

## 超文本标记语言

```html
<div class="words" contenteditable>
    <p id="p"></p>
</div>
```

我们使用**语音识别**对象将语音转换为文本，然后在屏幕上显示文本。

我们还增加了 **WebKit 语音识别**在谷歌 chrome 和苹果 safari 中进行语音识别。

## java 描述语言

```html
window.SpeechRecognition=window.SpeechRecognition 
    || window.webkitSpeechRecognition;
```

InterimResults 结果应返回 *true* ，默认值为 *false。*如此设置*中间结果=真*

## java 描述语言

```html
recognition.interimResults = true;
```

使用 **appendChild()** 方法追加一个节点作为节点的最后一个子节点。

## java 描述语言

```html
const words=document.querySelector('.words');
words.appendChild(p);
```

添加 eventListener，在这个事件 Listener 中， **map()** 方法用于创建一个新数组，结果是为每个数组元素调用一个函数。

**注:**此方法不改变原数组。

使用 **join()** 方法将数组作为字符串返回。

## java 描述语言

```html
recognition.addEventListener('result', e => {
    const transcript = Array.from(e.results)
        .map(result => result[0])
        .map(result => result.transcript)
        .join('')

    document.getElementById("p").innerHTML = transcript;
    console.log(transcript);
});
```

**最终代码:**

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">

    <title>Speech to Text</title>
</head>

<body>
    <div class="words" contenteditable>
        <p id="p"></p>
    </div>

    <script>
        var speech = true;
        window.SpeechRecognition = window.SpeechRecognition
                        || window.webkitSpeechRecognition;

        const recognition = new SpeechRecognition();
        recognition.interimResults = true;
        const words = document.querySelector('.words');
        words.appendChild(p);

        recognition.addEventListener('result', e => {
            const transcript = Array.from(e.results)
                .map(result => result[0])
                .map(result => result.transcript)
                .join('')

            document.getElementById("p").innerHTML = transcript;
            console.log(transcript);
        });

        if (speech == true) {
            recognition.start();
            recognition.addEventListener('end', recognition.start);
        }
    </script>
</body>

</html>
```

**输出:**

如果用户在运行文件后告诉“Hello World”，它会在屏幕上显示以下内容。

```html
Hello World
```