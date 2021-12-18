# Fabric.js max()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-max-method/](https://www.geeksforgeeks.org/fabric-js-max-method/)

**max()方法**用于从指定数组中寻找最大值。

**语法:**

```
max( array )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Array:** This parameter holds the array to be iterated.

**返回值:**此方法返回数组的最大值。

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
        console.log(fabric.util.array.max([5, 3, 9, 2]));
    </script>
</body>

</html>
```

输出:

```
9
```

**示例 2:** 在下面的代码中，为了找到最大值，考虑了字母表的 ascii 值。

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
        console.log(fabric.util.array.max(["a", "gfg"]));
    </script>
</body>

</html>
```

输出:

```
gfg
```

**参考:**T2】http://fabricjs.com/docs/fabric.util.array.html#.max