# 如何使用 JavaScript 创建上一个和下一个按钮以及非工作在结束位置？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 创建上一个和下一个按钮和非工作端位置/](https://www.geeksforgeeks.org/how-to-create-previous-and-next-button-and-non-working-on-end-position-using-javascript/)

任务是在 JavaScript 的帮助下创建上一个和下一个按钮，该按钮在结束位置不起作用。

在这里，当预**按钮**处于起始位置时，我们将添加**禁用**属性，对于我们来说是 1，当预【】按钮不处于起始(1)位置时，我们将移除**禁用**属性。

**下一个按钮**也是一样，当它在终点位置时增加**禁用**属性，对我们来说是 5，当它不在终点位置时删除**禁用**属性。这方面的执行情况如下:

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <style>
        .container {
            margin: 100px 400px;
        }

        .no-box {
            padding-left: 30px;
            font-size: 60px;
        }

        .btn {
            background-color: rgb(179, 179, 179);
        }

        .btn:hover {
            color: white;
            background-color: green;
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="no-box">
            <span class="no">1</span>
        </div>

        <button class="btn" onclick="prev()">
            prev
        </button>

        <button class="btn" onclick="next()">
            next
        </button>
    </div>

    <script>
        var no_box = document
            .querySelector('.no-box');

        var i = 1;

        function prev() {

            // Start position 
            if (i == 1) {

                // Add disabled attribute on
                // prev button
                document.getElementsByClassName(
                        'prev').disabled = true;

                // Remove disabled attribute 
                // from next button 
                document.getElementsByClassName(
                        'next').disabled = false;
            } else {
                i--;
                return setNo();
            }
        }

        function next() {

            // End position
            if (i == 5) {

                // Add disabled attribute on 
                // next button
                document.getElementsByClassName(
                        'next').disabled = true;

                // Remove disabled attribute
                // from prev button
                document.getElementsByClassName(
                        'prev').disabled = false;
            } else {
                i++;
                return setNo();
            }
        }

        function setNo() {

            // Change innerhtml
            return no_box.innerHTML = i;
        }
    </script>
</body>

</html>
```

**输出:**

<video class="wp-video-shortcode" id="video-513203-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20201112184927/bandicam-2020-11-12-18-48-58-626.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20201112184927/bandicam-2020-11-12-18-48-58-626.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20201112184927/bandicam-2020-11-12-18-48-58-626.mp4)</video>