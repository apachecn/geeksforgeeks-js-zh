# 什么是正确的 JSON 内容类型？

> 原文:[https://www . geesforgeks . org/什么是正确的 json 内容类型/](https://www.geeksforgeeks.org/what-is-the-correct-json-content-type/)

[**【内容类型】**](https://www.geeksforgeeks.org/http-headers-content-type/) 是一个 HTTP 头，用于指示资源的媒体类型，在响应的情况下，它告诉浏览器返回的内容的实际内容类型是什么。在任何 POST 或 PUT 请求的情况下，客户端会告诉服务器发送的数据类型。
为了知道浏览器将要遇到的内容类型，它会执行 MIME 嗅探。MIME 或多用途互联网邮件扩展是非文本电子邮件附件的规范。它允许邮件客户端或网络浏览器通过电子邮件发送和接收不同文件格式的附件。对于接收 JSON 请求，提及或告诉浏览器它将接收的请求类型是很重要的。所以我们通过在内容类型中提到它来设置它的 MIME 类型。我们可以通过两种方式做到这一点:

*   **MIME 类型:应用/json**
*   **MIME 类型:应用/javascript**

**MIME 类型:application/json**
在不知道如何使用这些数据时使用。当信息以 JSON 格式从服务器中提取时，它可能是通过链接或从任何文件中提取的，在这种情况下，它被使用。在这种情况下，客户端只获得 JSON 格式的数据，这些数据可以用作数据的链接，并且可以由任何前端框架实时格式化。

*   **示例:**在本例中，MIME 类型是**应用程序/json** ，因为它只是从该变量中提取字典，并将其置于 json 格式，然后显示出来。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// Setting the header
header('Content-Type:application/json');

// Initializing the directory
$dir =[
    ['Id'=> 1, 'Name' => 'Geeks' ],
    ['Id'=> 2, 'Name' => 'for'],
    ['Id'=> 3, 'Name' => 'Geeks'],
      ];
// Shows the json data
echo json_encode($dir);
?>
```

*   **输出:**

```
[{"Id":1, "Name":"Geeks"}, {"Id":2, "Name":"for"}, {"Id":3, "Name":"Geeks"}]
```

**MIME 类型:应用/javascript**
当数据的使用是预定义的时候使用。它由客户端 ajax 应用程序调用的应用程序使用。当数据类型为 JSON-P 或 JSONP 时使用。当应用编程接口封装在函数调用中时，使用带有填充的 JSONP 或 JavaScript 对象符号。该函数在客户端 JavaScript 代码中定义，API 作为参数传递给它，因此它充当可执行的 JavaScript 代码。

*   **示例:**在这个示例中，MIME 类型是 application/javascript，因为它只是从变量中提取字典，以 JSON 格式提取它，然后将其作为参数发送给客户端的函数调用。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Using application/javascript
header('Content-Type:application/javascript');
$dir =[
    ['Id'=> 1, 'Name' => 'Geeks' ],
    ['Id'=> 2, 'Name' => 'for'],
    ['Id'=> 3, 'Name' => 'Geeks'],
      ];

// Making a function call to the client side 
// using Function_call()
// Sending JSON data as a parameter to client.
echo "Function_call(".json_encode($dir).");";

?>
```

*   **输出:**

```
Function_call([{"Id":1, "Name":"Geeks"}, {"Id":2, "Name":"for"}, 
{"Id":3, "Name":"Geeks"}])
```

建议使用**应用/json** 代替**应用/javascript** ，因为 json 数据不被认为是 javascript 代码。它是一个标准，因此作为**应用程序/json** 被赋予一个单独的内容类型。