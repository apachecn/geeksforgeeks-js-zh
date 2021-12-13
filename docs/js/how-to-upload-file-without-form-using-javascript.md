# 如何用 JavaScript 上传没有表单的文件？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 上传无格式文件/](https://www.geeksforgeeks.org/how-to-upload-file-without-form-using-javascript/)

有几种方法可以在不使用 JavaScript 表单的情况下上传文件:

**方式一:**这种方式是使用**表单数据**，可以不使用任何一种表单上传文件。这种方法的特殊之处在于，网络方法(如 fetch)可以接受一个 FormData 对象作为主体。它被编码并与内容类型(多部分/表单数据)一起发送出去。

**JavaScript 代码片段:**

## JavaScript

```html
var gfg = new FormData();

gfg.append('pictureFile',
        pictureInput.files[0]);

// upload.php is the file to be uploaded
$.ajax({
    url: 'upload.php',
    type: 'POST',
    processData: false,
    contentType: false,
    dataType: 'json',
    data: gfg
});
```