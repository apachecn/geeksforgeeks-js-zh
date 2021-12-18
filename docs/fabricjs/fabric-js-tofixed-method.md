# Fabric.js toFixed()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-tofixed-method/](https://www.geeksforgeeks.org/fabric-js-tofixed-method/)

Fabric.js 中的 **toFixed()方法**用于将指定的分数转换为四舍五入的定数。

**语法:**

```
toFixed(number, fractionDigits)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数:**此参数保存分数。
*   **分数位数:**此参数保存指定分数小数点后要保留的分数位数。

**返回值:**此方法返回转换后的定数。

**例 1:**

## java 描述语言

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
        // Calling toFixed() function over
        // some specified fraction number
        console.log(fabric.util.toFixed(1234.567));
        console.log(fabric.util.toFixed(1234.567, 1));
        console.log(fabric.util.toFixed(1234.567, 2));
        console.log(fabric.util.toFixed(1234.567, 3));
        console.log(fabric.util.toFixed(1234.567, 4));
    </script>
</body>

</html>
```

**输出:**

```
1235
1234.6
1234.57
1234.567
1234.567
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

        // Specifying some fraction numbers
        var number1 = 0;
        var number2 = 123;
        var number3 = 0.789;

        // Specifying some fractionDigits
        var fractionDigits1 = 1;
        var fractionDigits2 = 2;

        // Calling toFixed() function over
        // the above specified fraction numbers
        // and fractionDigits
        console.log(fabric.util.toFixed(number1));
        console.log(fabric.util.toFixed(number2));
        console.log(fabric.util.toFixed(number2,
            fractionDigits1));
        console.log(fabric.util.toFixed(number3,
            fractionDigits1));
        console.log(fabric.util.toFixed(number3,
            fractionDigits2));
    </script>
</body>

</html>
```

**输出:**

```
0
123
123
0.8
0.79
```