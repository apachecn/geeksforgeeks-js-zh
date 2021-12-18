# JavaScript | WebAPI |文件|文件名属性

> 原文:[https://www . geesforgeks . org/JavaScript-web API-file-file-name-property/](https://www.geeksforgeeks.org/javascript-webapi-file-file-name-property/)

文件名属性是文件网络应用编程接口的一个内置函数，它给出了由文件对象表示的文件名。出于安全原因，此属性不包含文件路径。

**语法:**

```
var name = file.name;
```

**返回值:**返回一个字符串，包含没有路径的文件名。

**示例:**

```
<!DOCTYPE html>
<html>
    <head>
        <title>
            WebAPI File.name Property
        </title>

        <style>
            #main {
                padding: 10px;
                width: 300px;
                border: 1px solid green;
                text-align:center;
                font-size:22px;
            }
        </style>
    </head>

    <body>
        <div id = "main">
            <div>GeeksForGeeks</div>
            <div>file.name</div>
            <input type = "file" multiple onchange 
                = "myGeeks(this)">
        </div>

        <script type="text/javascript">

            function myGeeks(input_file) {
                var files = input_file.files;

                for (var i = 0; i < files.length; i++) {
                    alert("Name of file:" + files[i].name);
                }
            }
        </script>
    </body>
</html>                    
```

**输出:**
![](img/5ddd31606c2d190fb1babc22818f0c28.png)

**支持的浏览器:**WebAPI file . name 属性支持的浏览器如下:

*   边缘 12
*   谷歌 Chrome 13
*   Firefox 3.6
*   歌剧 16
*   Internet Explorer 10
*   旅行队

**参考:**T2】https://developer.mozilla.org/en-US/docs/Web/API/File/name