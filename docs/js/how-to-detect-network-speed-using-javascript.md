# 如何用 JavaScript 检测网速？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 检测网络速度/](https://www.geeksforgeeks.org/how-to-detect-network-speed-using-javascript/)

要使用 javascript 检测网络速度，我们将使用以下方法。

**方法:**打开你想知道连接速度的网页。该页面应该是您想要添加 javascript 代码来检测速度的页面。为变量分配或设置要用于速度测试的图像地址。应该创建用于存储测试开始时间、结束时间和下载大小的变量。设置相当于图像文件大小的“下载大小”(以字节为单位)。当图像下载完成时，下载动作的结束被指定为激活。它计算下载过程的速度，并将其转换为“kbps”和“mbps”。

下面是示例说明上述方法:
**示例:**

```
<!DOCTYPE html>
<html>
    <head>
        <title>
          To detect network speed using JavaScript
        </title>
    </head>
    <body>
        <script type="text/javascript">
            var userImageLink = 
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200714180638/CIP_Launch-banner.png";
            var time_start, end_time;

            // The size in bytes
            var downloadSize = 5616998;
            var downloadImgSrc = new Image();

            downloadImgSrc.onload = function () {
                end_time = new Date().getTime();
                displaySpeed();
            };
            time_start = new Date().getTime();
            downloadImgSrc.src = userImageLink;
            document.write("time start: " + time_start);
            document.write("<br>");

            function displaySpeed() {
                var timeDuration = (end_time - time_start) / 1000;
                var loadedBits = downloadSize * 8;

                /* Converts a number into string
                   using toFixed(2) rounding to 2 */
                var bps = (loadedBits / timeDuration).toFixed(2);
                var speedInKbps = (bps / 1024).toFixed(2);
                var speedInMbps = (speedInKbps / 1024).toFixed(2);
                alert("Your internet connection speed is: \n" 
                      + bps + " bps\n" + speedInKbps 
                      + " kbps\n" + speedInMbps + " Mbps\n");
            }
        </script>
    </body>
</html>
```

**输出:**
![](img/f6328dd890117085751a8a28375ebd2c.png)