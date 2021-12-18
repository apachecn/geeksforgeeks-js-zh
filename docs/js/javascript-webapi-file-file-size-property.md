# JavaScript | WebAPI | File | File . size 属性

> 原文:[https://www . geesforgeks . org/JavaScript-web API-file-file-size-property/](https://www.geeksforgeeks.org/javascript-webapi-file-file-size-property/)

file.name 属性是 file WebAPI 的一个内置函数，它以字节为单位给出文件的大小。

**语法:**

```
var size = instanceOfFile.size;
```

**返回值:**返回一个数字，包含文件的大小，以字节为单位。

**示例:**

```
<!DOCTYPE html>
<html>
<head>
    <title>
        WebAPI File.name
    </title>

    <style>
        #main {
            padding: 10px;
            width: 300px;
            border: 1px solid black;
            text-align:center;
            font-size:22px;
        }
    </style>
</head>

<body>
    <div id = "main">

        <div>GeeksforGeeks</div>
        <div>file.size</div>

        <input type = "file" multiple id = "file_input"
            onchange = "myGeeks(this)">
    </div>

    <script type="text/javascript">
        function myGeeks(fileInput) {

            // File input
            var fileInput = document.getElementById("file_input");

            var files = fileInput.files;

            for (var i = 0; i < files.length; i++) {
                alert(files[i].name + " has a size of "
                + files[i].size + " Bytes");
            }
        }
    </script>
    </body>
</html>                    
```

**输出:**
![](img/f4f95c34300456a5047ff50136398373.png)

**支持的浏览器:**WebAPI file . name 属性支持的浏览器如下:

*   边缘
*   谷歌 Chrome
*   火狐浏览器
*   歌剧
*   微软公司出品的 web 浏览器
*   旅行队

**参考:**T2】https://developer.mozilla.org/en-US/docs/Web/API/File/size