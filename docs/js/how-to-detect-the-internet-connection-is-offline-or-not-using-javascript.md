# 如何使用 JavaScript 检测互联网连接是否离线？

> 原文:[https://www . geesforgeks . org/如何检测互联网连接是否离线使用 javascript/](https://www.geeksforgeeks.org/how-to-detect-the-internet-connection-is-offline-or-not-using-javascript/)

在某些情况下，在执行所需任务之前，有必要确定浏览器是在线还是离线。许多开发人员使用 AJAX 通过向服务器发送请求来确定浏览器的连接状态(在线或离线)。但是，这不是确定浏览器状态的好方法，因为它需要带宽，还会影响可用性。

然而，JavaScript 的浏览器对象模型(BOM)提供了一种检测浏览器连接状态的直接方法，即浏览器是在线还是离线。

要执行此检查，针对所有可能的浏览器，我们将使用以下属性:

> **导航器. onLine**

**语法:**

```html
function isOnline() { 
    return ( navigator.onLine) 
}
```

**示例:**本示例显示一个按钮，如果点击该按钮，将显示连接状态。

```html
<!DOCTYPE html>
<html>

<body>

    <p>Click the button to check 
      if the browser is online.</p>

    <button onclick="isOnline()">
      Click Me
  </button>

    <p id="demo"></p>

    <script>
        function isOnline() {

            if (navigator.onLine) {
                document.getElementById(
                  "demo").innerHTML = "Online";
            } else {
                document.getElementById(
                  "demo").innerHTML = "Offline";
            }
        }
    </script>

</body>

</html>
```

**注意:**支持该属性的浏览器最低版本:

*   谷歌浏览器:14.0
*   互联网浏览器:是的
*   火狐:3.5
*   Safari: 5.0.4
*   歌剧:是的

**输出:**
![Output](img/7d1e508cb3e99b6c4ef2840ebd78c16b.png)