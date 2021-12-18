# 下划线. js _。迭代()函数

> 原文:[https://www . geesforgeks . org/下划线-js-_-迭代-函数/](https://www.geeksforgeeks.org/underscore-js-_-iteratee-function/)

**下划线. js** 是一个 JavaScript 库，它提供了很多有用的函数，在很大程度上有助于编程，比如映射、过滤、调用等。即使不使用任何内置对象。

**_。iteratee()函数**是一个内置在下划线中的函数，用于生成一个回调函数，可以应用于集合中的每个元素。此方法支持常见回调用例的多种速记语法，并根据值的类型返回输出。

**语法:**

```
_.iteratee( value, context )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **值:**是规定值。
*   **上下文:**是要使用的上下文。这是一个可选参数。

**返回值:**该方法根据值的类型返回输出。

**示例 1:** 在此示例中，该方法不使用任何参数。

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

        // Calling iteratee method with
        // no parameters
        console.log(_.iteratee());
    </script>
</body>

</html>
```

**输出:**

```
function(n){return n}
```

**示例 2:** 在该示例中，给该方法赋予了用户定义的函数。

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

        // Calling iteratee method
        // with its parameter
        console.log(
            _.iteratee(
                function (num) {
                    return num * 4;
                }
            )
        );
    </script>
</body>

</html>
```

**输出:**

```
function(num) { return num * 4; }
```

**示例 3:** 在本例中，键值对作为参数传递。

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

        // Calling iteratee method
        // with its parameter
        console.log(
            _.iteratee(
                { portal: 'GeeksforGeeks' }, []
            )
        );
    </script>
</body>

</html>
```

**输出:**

```
function(n){return h.isMatch(n,r)}

```

**示例 4:** 在本例中，字符串作为参数传递。

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
    <script>

        // Calling iteratee method with
        // its parameter
        console.log(
            _.iteratee('GfG', [])
        );
    </script>
</body>

</html>
```

**输出:**

```
function(n){return null==n?void 0:n[r]}
```