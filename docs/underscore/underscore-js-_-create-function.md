# 下划线. js _。创建()函数

> 原文:[https://www . geesforgeks . org/下划线-js-_-create-function/](https://www.geeksforgeeks.org/underscore-js-_-create-function/)

**下划线. js** 是一个 JavaScript 库，它提供了很多有用的函数，在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。create()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用于创建一个新的对象，该对象以所述的*原型*和*道具*作为其自身属性，并可选择附加。

**语法:**

```
_.create(prototype, props)
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **原型:**是要使用的原型。
*   **道具:**是所用原型的属性，可以随意附加。

**返回值:**这个方法返回一个新的对象。

**例 1:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        var author_article = [
            { author: 'Nidhi1352', articles: 792 }, 
            { author: 'Nisha95', articles: 590 }, 
            { author: 'Rohit01', articles: 450 }];

        // Calling create method with its parameter
        var obj = _.create(author_article.prototype, 
                    { author: "Rahul096" });
        console.log(obj);
    </script>
</body>

</html>
```

**输出:**

```
{"author":"Rahul096"}
```

**例二:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
    </script>
</head>

<body>
    <script>
        var array = [3, 4, 6, 8, 9]

        // Calling create method with its parameter
        var new_obj = _.create(array.prototype, [10]);
        console.log(new_obj);
    </script>
</body>

</html>
```

**输出:**

```
{"0":10}
```

**参考:**T2】https://underscorejs.org/#create