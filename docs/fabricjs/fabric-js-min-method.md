# 织物最小()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-min-method/](https://www.geeksforgeeks.org/fabric-js-min-method/)

**min()方法**用于从指定数组中寻找最小值。

**语法:**

```
min( array )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Array:** This parameter holds the array to be iterated.

**返回值:**该方法从数组中返回最小值。

**例 1:**

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        console.log(fabric.util.array.min([5, 3, 9, 2]));
    </script>
</body>

</html>
```

**输出:**

```
2
```

**示例 2:** 在下面的代码中，字母表的 ascii 值被考虑用于查找最小值。

## Javascript

```
<!DOCTYPE html>
<html>

<head>
    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <script type="text/javascript">
        console.log(fabric.util.array.min(["a", "gfg"]));
    </script>
</body>

</html>
```

**输出:**

```
a
```

**参考:**T2】http://fabricjs.com/docs/fabric.util.array.html#.min