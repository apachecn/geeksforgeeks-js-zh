# Fabric.js removeFromArray()方法

> 原文:[https://www . geesforgeks . org/fabric-js-remove from array-method/](https://www.geeksforgeeks.org/fabric-js-removefromarray-method/)

**removeFromArray()方法**用于从指定的值数组中移除一个值。

**语法:**

```
removeFromArray(array, value)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存指定的值数组。
*   **值:**该参数保存将要从数组中删除的值。

**返回值:**这个方法返回剩余值的数组。

**例 1:**

## java 描述语言

```
<!DOCTYPE html>

<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>

    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
    </script>

    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Calling removeFromArray() function over
        // some specified arrays and values to be removed
        console.log(fabric.util.removeFromArray([1, 2, 3], 2));
        console.log(fabric.util.removeFromArray([1, 2, 3], 1));
        console.log(fabric.util.removeFromArray([1, 2, 3], 0));
    </script>
</body>

</html>
```

**输出:**

```
[1,3]
[2,3]
[1,2,3]
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>

<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>

    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
    </script>

    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Specifying some arrays
        var array1 = [2, 4, 6];
        var array2 = [1, 3, 4];

        // Specifying some values
        var value1 = 2;
        var value2 = 4;

        // Calling removeFromArray() function over the
        // above specified arrays and values to be removed
        console.log(fabric.util.removeFromArray(array1, value1));
        console.log(fabric.util.removeFromArray(array2, value2));
    </script>
</body>

</html>
```

**输出:**

```
[4,6]
[1,3]
```