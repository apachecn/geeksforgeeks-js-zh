# JavaScript 中 array.size()和 array.length 的区别

> 原文:[https://www . geesforgeks . org/数组大小与数组长度之差是多少 javascript/](https://www.geeksforgeeks.org/what-is-the-difference-between-array-size-and-array-length-in-javascript/)

**array.size()方法**在功能上等同于 **[array.length 属性](https://www.geeksforgeeks.org/javascript-array-length-property/)** ，只能在 **[jQuery](https://www.geeksforgeeks.org/jquery-tutorials/)** 中使用。这里在 JavaScript 中 **array.size()** 是无效的方法，所以应该使用 **array.length 属性**。

以下示例实现了上述概念:

**示例 1:** 本示例演示 array.size()方法和 array.length 属性。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Difference between array.size() method
        and array.length property
    </title>
</head>

<body>
    <p>
        Click the button to display
        the length of array.
    </p>

    <button onclick="findLength()">
        Try it
    </button>

    <p>
        Length of the array is: 
        <span id="demo"></span>
    </p>

    <script>
        var arr = ['geeks', 'for', 'geeks'];

        function findLength() {
            document.getElementById("demo").innerHTML
                        = arr.length;

            document.getElementById("demo").innerHTML
                        = arr.size();
        }
    </script>
</body>

</html>
```

**输出:**

```
Length of the array is: 3
error on console: TypeError: arr.size is not a function

```

**注意:****array . length 属性**为具有数值索引值的数组返回 last_key+1 的值。这个属性不能保证找到数组中的项数。

**示例 2:** 本示例显示 Array.length 属性的工作原理。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Array.length property
    </title>
</head>

<body>
    <p>
        Click the button to display
        the length of array.
    </p>

    <button onclick="findLength()">
        Try it
    </button>

    <p>
        Length of array the is: 
        <span id="demo"></span>
    </p>

    <script>
        var arr = ['geeks', 'for', 'geeks'];
        arr[50] = 'article';

        function findLength() {
            document.getElementById("demo")
                        .innerHTML = arr.length;
        }
    </script> 
</body>

</html>
```

**输出:**

```
Length of the array is: 51
```

**示例 3:** 本示例显示当索引键为非数字时，array.length 属性如何工作。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        array.length property with
        non-numeric index key
    </title>
</head>

<body>
    <p>
        Click the button to display
        the length of array.
    </p>

    <button onclick="findLength()">
        Try it
    </button>

    <p>
        Length of array the is: 
        <span id="demo"></span>
    </p>

    <script>
        var arr = new Array();
        arr['a'] = 1;
        arr['b'] = 2;
        arr['c'] = 3;

        function findLength() {
            document.getElementById("demo")
                    .innerHTML = arr.length;
        }
    </script> 
</body>

</html>
```

**输出:**

```
Length of the array is: 0
```