# 下划线. js _。restArguments()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-restarguments-function/](https://www.geeksforgeeks.org/underscore-js-_-restarguments-function/)

**下划线. js** 是一个 JavaScript 库，它提供了很多有用的函数，在很大程度上有助于编程，比如映射、过滤、调用等。即使不使用任何内置对象。

**_。restArguments()函数**是一个内置于下划线. js JavaScript 库中的函数，用于查找函数的一个版本，当调用该版本时，该版本可以接收来自所述 *startIndex* 的所有参数，并将其收集到一个数组中。当没有给定值时，函数的参数数量将用于确定*开始指数*。

**语法:**

```
_.restArguments( function, startIndex )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **功能:**是规定的功能。
*   **开始索引:**是静止参数的开始位置。这是一个可选参数。

**返回值:**该方法返回一个函数版本，该版本在被调用时可以从指定的索引中接收所有参数。

**示例 1:** 在该示例中，使用了用户定义的函数。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://unpkg.com/underscore@1.11.0/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        // Calling restArguments method
        // with its parameter
        var writes =
            _.restArguments(function (authors, portal) {
                return authors + portal;
            });

        // Calling write with its values 
        console.log(
            writes(
                ['Nidhi1352', ' GeeksforGeeks!']
            )
        );
    </script>
</body>

</html>
```

**输出:**

```
Nidhi1352, GeeksforGeeks!
```

**示例 2:** 在此示例中，起始索引与用户定义的函数一起传递。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://unpkg.com/underscore@1.11.0/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        // Calling restArguments method
        // with its parameter
        var writes =
            _.restArguments(
                function (authors, portal, articles) {
                    return authors + portal + articles;
                }, [2]);

        // Calling writes with its values 
        console.log(
            writes(
                ['Nidhi1352', ' GeeksforGeeks!', ' 700 ']
            )
        );
    </script>
</body>

</html>
```

**输出:**

```
Nidhi1352, GeeksforGeeks!, 700 undefined
```

**例 3:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://unpkg.com/underscore@1.11.0/underscore-min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        var call =
            _.restArguments(function (who, whom) {
                return who + ' ' +
                    _.initial(whom).join(', ') +
                    (_.size(whom) > 2 ? ', & ' : '') +
                    _.last(whom);
            });

        // Calling the function above
        // with its values
        console.log(
            call(
                'She called', 'me', 'her', 'you.'
            )
        );
    </script>
</body>
```

**输出:**

```
She called me, her, & you.
```