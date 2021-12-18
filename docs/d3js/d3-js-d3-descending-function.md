# D3.js | d3.descending()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-descending-function/](https://www.geeksforgeeks.org/d3-js-d3-descending-function/)

D3.js 中的 **d3.descending()函数**是一个自然逆序的比较器函数，如果以降序取两个参数，返回-1，如果以升序取两个参数，返回 1，如果取两个相等的参数，返回 0。

**语法:**

```
d3.descending(a, b)
```

**参数:**该功能接受参数 **a、b** ，任意两个值。

**返回值:**按降序取两个参数(第一个参数大于第二个参数)返回-1，按升序取两个参数(第二个参数大于第一个参数)返回 1，取两个相等的参数返回 0。

下面的程序说明了 D3.js 中的 d3.descending()函数。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.descending() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling to d3.descending() function with 
        // two integer value parameters
        A = d3.descending(50, 20);
        B = d3.descending(2, 5);
        C = d3.descending(5, 5);

        // Getting the results
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        console.log(A);
    </script>
</body>

</html>                    
```

**输出:**

```
-1
1
0
```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.descending() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling to d3.descending() function with 
        // some alphabetical parameters
        A = d3.descending();
        B = d3.descending("a", "b");
        C = d3.descending("b", "a");
        D = d3.descending("b", "b");
        E = d3.descending("b");

        // Getting the results
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        document.write(D + "<br>");
        document.write(E + "<br>");
    </script>
</body>

</html>                    
```

**输出:**

```
NaN
1
-1
0
NaN
```

**注意:**如果该函数将字母作为参数，它会以 ascii 形式考虑它们，并相应地评估结果，如果给定的参数与其参数的格式不匹配，则它会返回 NaN，即 Not a Number。

**参考:**T2】https://devdocs.io/d3~5/d3-array#descending