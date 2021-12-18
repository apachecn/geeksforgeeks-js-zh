# 下划线. js _。绑定()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-绑定-函数/](https://www.geeksforgeeks.org/underscore-js-_-bind-function/)

_。bind()函数用于将函数绑定到对象。当函数被调用时，它的值将是对象。

**语法:**

```
_.bind(function, object, *arguments)
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **功能:**该参数保存需要执行的功能。
*   **对象:**该参数保存对象元素。
*   **参数:**这个参数需要在元素之间添加一些符号。

**返回值:**返回将函数绑定到对象的值。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        var fun = function (Geeks) {
            return 'Company Name : ' + this.Company
                + '\nAddress : ' + this.Address
                + '\nContact : ' + this.Contact
        };

        fun = _.bind(fun, {
            Company: 'GeeksforGeeks',
            Address: 'Noida',
            Contact: '+91 9876543210'
        });

        console.log(fun());
    </script>
</body>

</html>
```

**输出:**
![](img/9617c55ebf909ca2cf76da87435a4839.png)

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        var obj = {
            Name: "GeeksforGeeks",
            Address: "Noida"
        };

        var fun = function (Geeks) {
            return 'Welcome to ' + this.Name
                + '\nAddress: ' + this.Address
        };

        fun = _.bind(fun, obj);

        console.log(fun());
    </script>
</body>

</html>
```

**输出:**
![](img/1b905f2055c87603689bbabbe61a3a64.png)