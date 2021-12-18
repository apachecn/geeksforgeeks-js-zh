# JavaScript 数组填充()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-fill-method-2/](https://www.geeksforgeeks.org/javascript-array-fill-method-2/)

下面是用单个数字填充的**数组填充()**方法的例子。

*   **例:**

## Java Script 语言

```
<script>
    // JavaScript code for fill() method
    function func() {
        var arr = [1, 23, 46, 58];

        // fill array with 87
        arr.fill(87);
        document.write(arr);
    }
    func();
</script>
```

*   **输出:**

```
[87, 87, 87, 87]
```

**arr.fill()** 方法用于用给定的静态值填充数组。该值可用于填充整个数组，也可用于填充数组的一部分。
**语法:**

```
arr.fill(value, start, end)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **值:**定义数组元素替换的静态值。
*   **start(可选):**它定义了开始索引，数组将从该索引开始填充静态值。如果未定义该值，则起始指数取为 **0** 。如果起点为负，则净起点指数为**长度+起点**。
*   **end(可选):**该参数定义了数组中最后一个要填充静态值的索引。如果未定义该值，则默认情况下，最后一个索引，即**arr . length–1**将作为结束值。如果终点为负，则净终点定义为**长度+终点**。

**返回值:**此方法不返回新数组。而不是修改应用此方法的数组。
以下示例说明了 JavaScript 中的**数组填充()**方法:

*   **示例 1:** 在本示例中，方法 **fill()** 用 **87** 填充整个数组，替换数组中存在的所有初始值。

```
var arr = [1, 23, 46, 58];
arr.fill(87); 
```

**输出:**

```
[87, 87, 87, 87]
```

*   **示例 2:** 在本示例中，方法 **fill()** 用 **87** 填充从索引 **1** 到 **2** 比上部索引小一的数组，替换数组中存在的所有初始值。

```
var arr = [1, 23, 46, 58];
arr.fill(87, 1, 3); 
```

**输出:**

```
[1, 87, 87, 58]
```

*   **示例 3:** 在本示例中，方法 **fill()** 用 **87** 填充从索引 **1** 到 **3** 的数组，替换数组中存在的所有初始值。

```
var arr = [1, 23, 46, 58];
arr.fill(87, 2); 
```

**输出:**

```
[1, 23, 87, 87]
```

上述方法的代码定义如下:
**程序 1:**

## Java Script 语言

```
<script>
    // JavaScript code for fill() method
    function func() {
        var arr = [1, 23, 46, 58];

        // Here value = 87, start index=1
        arr.fill(87, 2);
        document.write(arr);
    }

    func();
</script>
```

**输出:**

```
[1, 23, 87, 87]
```

**节目 2:**

## Java Script 语言

```
<script>
    // JavaScript code for fill() method
    function func() {
        var arr = [1, 23, 46, 58];

        // here value = 87, start index=1 and
        // and last index = 3
        arr.fill(87, 1, 3);
        document.write(arr);
    }

    func();
</script>
```

**输出:**

```
[1, 87, 87, 58]
```

**支持的浏览器:**JavaScript**数组填充()**方法支持的浏览器如下:

*   谷歌 Chrome 45.0
*   微软边缘 12.0
*   Mozilla Firefox 31.0
*   Safari 7.1
*   Opera 32.0