# JavaScript dataview . getfloat 64()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-dataview-get float 64/

下面是 **DataView.getFloat64()** 方法的例子。

*   **示例:**当一个正浮点数作为参数传递时

## java 描述语言

```
<script>
    var buffer = new ArrayBuffer(20);
    var dataview1 = new DataView(buffer, 0, 10);
    dataview1.setFloat64(1, 12.01);
    document.write(dataview1.getFloat64(1) + "<br>");
</script>
```

*   **输出:**

```
12.01
```

**dataView.getFloat64()** 是 dataView 中的一个内置函数，用于在指定位置(即距数据视图开始的字节偏移量)获取 64 位浮点。64 位浮点数的取值范围为-1.7E+308 到+1.7E+308
**语法:**

```
dataView.getFloat64(byteOffset)
```

**参数:**它有一个字节偏移的参数 byteOffset，它表示从视图开始读取数据。
**返回值:**返回 64 位有符号浮点数。
**例 1:**

```
Input: dataview1.setFloat64(1, 56.34); 
Output: 56.34
```

**例 2:**

```
Input: dataview1.setFloat64(1, Math.PI);
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
    dataview1.setFloat64(1, 56.34);
    document.write(dataview1.getFloat64(1) + "<br>");

</script>
```

**输出:**

```
56.34
```

**代码#2:**
不仅有浮点值，还有像 math 这样的数学函数。PI 可以作为函数的参数。

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view with slot from o to 10
    var dataview1 = new DataView(buffer, 0, 10);

    // put the value of PI at slot 1
    dataview1.setFloat64(1, Math.PI);
    document.write(dataview1.getFloat64(1) + "<br>");

</script>
```

**输出:**

```
3.1415927410125732
```

**代码#3:**
当没有任何数据用于存储时，它返回 NaN，即不是一个数字。

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view
    var dataview1 = new DataView(buffer, 0, 10);

    // putting no data at slot 1
    dataview1.setFloat64(1);
    document.write(dataview1.getFloat64(1) + "<br>");

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