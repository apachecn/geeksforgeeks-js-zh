# D3.js | d3.range()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-range-function/](https://www.geeksforgeeks.org/d3-js-d3-range-function/)

D3.js 中的 **d3.range()函数**用于返回一个数组，该数组包含从 **start** 参数开始的算术级数，并在一个称为**步骤**的均匀间隔数值序列上迭代，以 **stop** 参数结束。
**语法:**

```
d3.range(start, stop, step)
```

**参数:**该函数接受三个参数，如下图所示:-

*   **start:** 是包含整数值，是输出数组的第一个元素。其默认值为 0。
*   **stop:** 是不加入输出数组的独占整数值。
*   **步骤:**它是整数值，定期与起始值相加，并打印结果，直到停止值到达。

**返回值:**返回一个包含算术级数的数组。
下面的程序说明了 D3.js 中的 d3.range()函数
**示例 1:**

## java 描述语言

```
<body>
    <script src='https://d3js.org/d3.v4.min.js'></script>

    <script>

        // Calling to d3.range() function
        // with parameters start, stop and steps.
        A = d3.range(0, 4, 1);
        B = d3.range(10, 100, 10);
        C = d3.range(5, 50, 5);
        D = d3.range(1, 10, 2);

        // Getting an array of arithmetic progression
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        document.write(D + "<br>");
    </script>
</body>
```

**输出:**

```
[0,1,2,3]
[10,20,30,40,50,60,70,80,90]
[5,10,15,20,25,30,35,40,45]
[1,3,5,7,9]
```

**例 2:**

## java 描述语言

```
<body>
    <script src='https://d3js.org/d3.v4.min.js'></script>

    <script>

        // Calling to d3.range() function
        // with parameters start, stop and steps.
        A = d3.range(1, 2);
        B = d3.range(10, 20);
        C = d3.range(0, 10, 0.5);
        D = d3.range(1, 10, 0.9);

        // Getting an array of arithmetic progression
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        document.write(D + "<br>");
    </script>
</body>
```

**输出:**

```
1
[10,11,12,13,14,15,16,17,18,19]
[0,0.5,1,1.5,2,2.5,3,3.5,4,4.5,5,5.5,6,6.5,7,7.5,8,8.5,9,9.5]
[1,1.9,2.8,3.7,4.6,5.5,6.4,7.3,8.2,9.1]
```

**注意:**在上面的代码中，部分 range()函数没有取步长值，因此其默认值被认为是 1。
T3【参考:T5【https://devdocs.io/d3~5/d3-array#range】T6