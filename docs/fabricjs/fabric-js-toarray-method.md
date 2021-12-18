# Fabric.js toArray()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-toarray-method/](https://www.geeksforgeeks.org/fabric-js-toarray-method/)

Fabric.js 中的 **toArray()方法**用于将指定的类数组对象转换为数组。这可用于将参数列表或节点列表转换为数组。

**语法:**

```
toArray( arrayLike )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **类数组:**此参数保存指定的类数组对象。

**返回值:**这个方法返回转换后的数组。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Calling toArray() function over
        // some specified array-like objects
        console.log(fabric.util.toArray(1));
        console.log(fabric.util.toArray(1, 2));
        console.log(fabric.util.toArray([1, 2, 3, 4]));
        console.log(fabric.util.toArray("a"));
        console.log(fabric.util.toArray("a", "b"));
        console.log(fabric.util.toArray(["a", "b", "c"]));
    </script>
</body>

</html>
```

**输出:**

```
[]
[]
[1,2,3,4]
["a"]
["a"]
["a","b","c"]
```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Specifying some array-like objects
        var number1 = 0;
        var number2 = 123;
        var number3 = (1, 2);
        var number4 = [1, 2, 3, 4];

        // Calling toArray() function over
        // the above specified array-like objects
        console.log(fabric.util.toArray(number1));
        console.log(fabric.util.toArray(number2));
        console.log(fabric.util.toArray(number3));
        console.log(fabric.util.toArray(number4));
    </script>
</body>

</html>
```

**输出:**

```
[]
[]
[]
[1,2,3,4]
```