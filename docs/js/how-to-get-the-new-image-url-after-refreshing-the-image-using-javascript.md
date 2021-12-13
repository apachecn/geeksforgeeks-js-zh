# 使用 JavaScript 刷新图像后如何获取新的图像 URL？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 刷新图像后获取新图像-URL/](https://www.geeksforgeeks.org/how-to-get-the-new-image-url-after-refreshing-the-image-using-javascript/)

浏览器缓存依赖图像 URL 来决定图像是否相同以及是否使用存储的版本。这意味着，如果我们更改了网址中的某些内容，然后试图重新加载图像，缓存将不再能够更改它是相同的资源。缓存将再次从服务器获取它。

**方法:**要在不影响图像的情况下更改 URL，可以更改可以附加到 URL 末尾的参数。参数必须是唯一的。我们可以使用时间戳，网址将始终是唯一的。

为了在 JavaScript 中刷新图像，我们可以简单地选择 *img* 元素，并将其 src 属性修改为目标图像的属性，以及时间戳参数，以确保它不会从缓存中访问它。

**示例:**

```html
<!DOCTYPE html>
<html>

<head>
    <title>Refresh Image</title>
</head>

<body>
    <!-- Display the image -->
    <img id="gfgimage" src="bg.png" 
        height="500" width="700" />

    <script>
        // Create a timestamp
        var timestamp = new Date().getTime();

        // Get the image element 
        var image = document.getElementById("gfgimage");

        // Adding the timestamp parameter to image src
        image.src = "bg.png?t=" + timestamp;
        console.log(image.src);
    </script>
</body>

</html>
```

**输出:**
![Image URL before refresh](img/e609c16983e6dc1fca5dc1e1e980a0d8.png)

现在，即使图像被新图像替换，它也会加载新图像。一般来说，这可能会有一些性能问题，因为它不会使用缓存中的映像，并且必须始终使用服务器中的映像。