# 如何用 JavaScript 进行 ajax 调用？

> 原文:[https://www . geesforgeks . org/如何从 javascript 调用 Ajax/](https://www.geeksforgeeks.org/how-to-make-ajax-call-from-javascript/)

[Ajax](https://www.geeksforgeeks.org/ajax-introduction/) 代表异步 JavaScript 和 XML。它用于与服务器进行异步通信。Ajax 用于从服务器读取数据并更新页面或将数据发送到服务器，而不会影响当前的客户端页面。Ajax 是一个编程概念。

下面是一些用 JavaScript 进行 Ajax 调用的方法。

**方法 1:** 在这个方法中，我们将使用 [XMLHttpRequest 对象](https://www.geeksforgeeks.org/ajax-full-form/)进行 Ajax 调用。**[**XMLHttpRequest()**](https://www.geeksforgeeks.org/how-to-make-put-request-using-xmlhttprequest-by-making-custom-http-library/)方法创建 XMLHttpRequest 对象，用于向服务器发出请求。**

****语法:****

```
var xhttp = new XMLHttpRequest();
```

**上面的语法用于创建 XMLHttpRequest 对象。该对象有许多不同的方法，用于与服务器交互，以发送、接收或中断来自服务器的响应。在响应中，我们从服务器获得一个字符串并打印出来。**

****示例:****

## **java 描述语言**

```
<script>
    function run() {

        // Creating Our XMLHttpRequest object
        var xhr = new XMLHttpRequest();

        // Making our connection 
        var url = 'https://jsonplaceholder.typicode.com/todos/1';
        xhr.open("GET", url, true);

        // function execute after request is successful
        xhr.onreadystatechange = function () {
            if (this.readyState == 4 && this.status == 200) {
                console.log(this.responseText);
            }
        }
        // Sending our request
        xhr.send();
    }
    run();
</script>
```

****输出:****

```
"{
  "userId": 1,
  "id": 1,
  "title": "delectus aut autem",
  "completed": false
}"
```

****方法 2:** 在这种方法中，我们将使用 jQuery 进行 ajax 调用。在 jQuery 中使用 [**ajax()**](https://www.geeksforgeeks.org/jquery-ajax-method/) 方法进行 ajax 调用。它被用来替代所有不支持 ajax 调用的方法。**

****语法:****

```
$.ajax({arg1: value, arg2: value, ... });
```

****参数:**它需要一个配置文件来配置 URL、类型、当我们得到响应或如果出错时要调用的函数等。**

****示例:****

## **超文本标记语言**

```
<!DOCTYPE HTML>
<html>

<head>
    <script src=
"https://code.jquery.com/jquery-3.6.0.min.js">
    </script>
</head>

<body>

    <script>

        function ajaxCall() {
            $.ajax({

                // Our sample url to make request
                url:
    'https://jsonplaceholder.typicode.com/todos/1',

                // Type of Request
                type: "GET",

                // Function to call when to
                // request is ok
                success: function (data) {
                    var x = JSON.stringify(data);
                    console.log(x);
                },

                // Error handling
                error: function (error) {
                    console.log(`Error ${error}`);
                }
            });
        }
        ajaxCall();
    </script>
</body>

</html>
```

****输出:****

```
{
  "userId": 1,
  "id": 1,
  "title": "delectus aut autem",
  "completed": false
}
```

****方法 3:** 在这个方法中，我们将使用[**fetch()**](https://www.geeksforgeeks.org/fetch-api/)**API，该 API 用于与服务器进行 XMLHttpRequest。由于结构灵活，使用方便。该应用编程接口向服务器发出请求，并获得结果作为[承诺](https://www.geeksforgeeks.org/javascript-promises/)，该承诺被解析为字符串。****

******语法:******

```
**fetch(url, {config}).then().catch();**
```

******参数:**以请求的网址和配置为参数。****

****我们将配置所需的数据，并向服务器发出请求。由于这是一个已解决的承诺，我们使用 [**然后()**](https://www.geeksforgeeks.org/why-we-use-then-method-in-javascript/) 函数和 **catch()** 函数为结果创建输出。作为回应，我们得到我们打印的字符串。****

******示例:******

## ****java 描述语言****

```
**<script>

    // Url for the request
    var url = 'https://jsonplaceholder.typicode.com/todos/1';

    // Making our request
    fetch(url, { method: 'GET' })
        .then(Result => Result.json())
        .then(string => {

            // Printing our response
            console.log(string);

            // Printing our field of our response
            console.log(`Title of our response :  ${string.title}`);
        })
        .catch(errorMsg => { console.log(errorMsg); });
</script>**
```

******输出:******

```
**{ userId:1 ,id:1 ,title : "delectus aut autem" ,completed : false
__proto__:Object }
Title of our response :  delectus aut autem**
```