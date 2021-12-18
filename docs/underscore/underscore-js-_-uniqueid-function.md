# 下划线. js _。uniqueId()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-uniqueid-function/](https://www.geeksforgeeks.org/underscore-js-_-uniqueid-function/)

**下划线. js** 是一个 JavaScript 库，它提供了许多有用的函数，这些函数在很大程度上有助于编程，比如映射、过滤、调用等，甚至不使用任何内置对象。

**_。uniqueId()函数**是 JavaScript 的下划线. js 库中的一个内置函数，用于为客户端模型或需要的 DOM 元素生成一个全局唯一的 Id。当一个前缀作为参数传递给这个方法时，生成的 id 将被附加到它上面。

**语法:**

```
_.uniqueId( prefix )

```

**参数:**如上所述，它接受单个参数，如下所述:

*   **前缀:**是附加到 id 的前缀，是可选参数。

**返回值:**这个方法返回一个全局唯一的 id。

**例 1:**

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

        // Using _.uniqueId() method 
        // with its parameter
        console.log(_.uniqueId('gfG_'));
        console.log(_.uniqueId('Geeks_'));
        console.log(_.uniqueId('CS_'));
    </script>
</body>

</html>
```

**输出:**

```
gfG_1
Geeks_2
CS_3
```

**例 2:**

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

        // Using a loop
        for (i = 3; i < 100; i *= 2) {

            // Calling uniqueId method
            // without any parameter   
            console.log(_.uniqueId());
        }
    </script>
</body>

</html>
```

**输出:**

```
1
2
3
4
5
6

```