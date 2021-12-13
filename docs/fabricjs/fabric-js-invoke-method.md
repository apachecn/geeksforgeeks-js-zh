# Fabric.js 调用()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-invoke-method/](https://www.geeksforgeeks.org/fabric-js-invoke-method/)

**invoke()方法**用于执行某些操作，如排序、连接等。在指定数组的元素上。

**语法:**

```html
invoke(array, method)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存要迭代的数组。
*   **方法:**该参数保存要调用的方法的名称。

**返回值:**该方法返回给定方法应用后形成的数组。

**例 1:**

## java 描述语言

```html
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
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
            console.log(fabric.util.array
            .invoke([[1, 6, 8], [7, 5, 3],
            [33, 76, 55]], 'sort'));
    </script>
</body>

</html>
```

**输出:**

```html
[[1, 6, 8], [3, 5, 7], [33, 55, 76]]
```

**例 2:**

## java 描述语言

```html
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
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
        console.log(fabric.util.array
            .invoke([[11, 6, 8], 
            [33, 25, 32]], 'join'));
    </script>
</body>

</html>
```

**输出:**

```html
["11, 6, 8", "33, 25, 32"]
```