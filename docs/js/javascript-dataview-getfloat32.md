# JavaScript dataview . getfloat 32()方法

> 哎哎哎::1230【https://www . geeksforgeeks . org/JavaScript-dataview-get float 32/

下面是 **dataView.getFloat32()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
    var buffer = new ArrayBuffer(20);
    var dataview1 = new DataView(buffer, 0, 10);
    dataview1.setFloat32(1, 12.01);
    document.write(dataview1.getFloat32(1) + "<br>");
</script>
```

*   **输出:**

```
12.010000228881836
```

**dataView.getFloat32()** 是 dataView 中的一个内置函数，用于在指定位置(即从 dataView 开始的字节偏移量)获取 32 位浮点。32 位浮点数的取值范围为-3.4E+38 到+3.4E+38
**语法:**

```
dataView.getFloat32(byteOffset)
```

**参数:**它有一个字节偏移的参数 byteOffset，它表示从视图的开始(开始)读取数据的位置。
**返回值:**返回 32 位有符号浮点数。
**例 1:**

```
Input: dataview1.setFloat32(1, 56.34);
Output: 56.34000015258789
```

**例 2:**

```
Input: dataview1.setFloat32(1, Math.PI);
Output: 3.1415927410125732
```

**JavaScript 代码展示此方法的工作原理:**
**代码#1:**

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view
    var dataview1 = new DataView(buffer, 0, 10);

    // put the data 56.34 at slot 1
    dataview1.setFloat32(1, 56.34);
    document.write(dataview1.getFloat32(1) + "<br>");

</script>
```

**输出:**

```
56.34000015258789
```

**代码#2:** 不仅是浮点值，还有像 math 这样的数学函数。PI 可以作为函数的参数。

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view with slot from o to 10
    var dataview1 = new DataView(buffer, 0, 10);

    // put the value of PI at slot 1
    dataview1.setFloat32(1, Math.PI);
    document.write(dataview1.getFloat32(1) + "<br>");

</script>
```

**输出:**

```
3.1415927410125732
```

**代码#3:** 当没有要存储的数据时，则返回 NaN，即不是数字。

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view
    var dataview1 = new DataView(buffer, 0, 10);

    // putting no data at slot 1
    dataview1.setFloat32(1);
    document.write(dataview1.getFloat32(1) + "<br>");

</script>
```

**输出:**

```
NaN
```

**支持的浏览器:**

*   谷歌 Chrome 9 及以上版本
*   边缘 12 及以上
*   Firefox 15 及以上版本
*   Internet Explorer 10 及以上版本
*   Opera 12.1 及以上
*   Safari 5.1 及以上版本