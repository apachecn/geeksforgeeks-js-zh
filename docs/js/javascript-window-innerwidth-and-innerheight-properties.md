# JavaScript |窗口内宽和内高属性

> 原文:[https://www . geesforgeks . org/JavaScript-window-inner width-and-inner height-properties/](https://www.geeksforgeeks.org/javascript-window-innerwidth-and-innerheight-properties/)

JavaScript 中的 innerWidth 属性返回宽度，innerHeight 属性返回窗口内容区域的高度。

**语法:**

```
window.innerWidth
window.innerHeight
```

**参数:**不需要任何参数。

**返回值:**返回一个数字，代表窗口内容区域的宽度和高度。

**注意:**对于 IE 8 即互联网 Edg 8 或更早版本，使用 clientWidth 和 clientHeight 获取窗口的宽度和高度。

**示例:**

```
<!DOCTYPE html>
<html>
     <head>
          <title>Browser Inner width and height</title>
          <style>
            body{
                text-align:center;
            }
            .gfg {
                font-size:40px;
                font-weight:bold;
                color:green;
            }
          </style>
     </head>
     <body>
     <div class = "gfg">GeeksforGeeks</div>
     <h2>Browser Window</h2>
     <p id="demo"></p>
     <script>
          var Width, Height, result;

          // height and width of Browser window
          Width = window.innerWidth || document.documentElement.clientWidth
                  || document.body.clientWidth;

          Height = window.innerHeight || document.documentElement.clientHeight
                  || document.body.clientHeight;
          // Display Width and Height.
          result = document.getElementById("demo");
          result.innerHTML = "Browser inner width: " + Width +
                              "<br>Browser inner height: " + Height;

     </script>
</body>
</html>
```

**输出:**
![](img/ef1fd1a33b6142b4741498f015362d80.png)