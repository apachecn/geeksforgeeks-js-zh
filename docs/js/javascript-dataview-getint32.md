# JavaScript dataView.getInt32()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-dataview-getint 32/

下面是 **dataView.getFloat32()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
    var buffer = new ArrayBuffer(20);
    var dataview1 = new DataView(buffer, 0, 10);
    dataview1.setInt32(1, 12);
    document.write(dataview1.getInt32(1) + "<br>");

</script>
```

*   **输出:**

```
12
```

**dataView.getInt32()** 是 dataView 中的一个内置函数，用于在指定位置(即从 dataView 开始的字节偏移量)获取 32 位整数。32 位整数值的范围是 0 到 4，294，967，295(无符号)，2，147，483，648 到 2，147，483，647(有符号整数值)。
**语法:**

```
dataview.getInt32(byteOffset)
```

**参数:**它有一个字节偏移的参数 byteOffset，它表示从视图开始读取数据。
**返回值:**返回 32 位有符号整数值。
**例 1:**

```
Input: dataview1.setInt32(1, 56); 
       document.write(dataview1.getInt32(1));
Output: 56
```

**例 2:**

```
Input: dataview1.setInt32(1, 4.5); 
       document.write(dataview1.getInt32(1)); 
Output: 4
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

    // put the data 56 at slot 1
    dataview1.setInt32(1, 56);
    document.write(dataview1.getInt32(1) + "<br>");

</script>
```

**输出:**

```
56
```

**代码#2:**
这里可以看出，这个函数不取浮点值，当这个浮点值被赋予这个函数时，它就把这个值转换成整数值。

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view with slot from o to 10
    var dataview1 = new DataView(buffer, 0, 10);

    // put the 4.5 at slot 1
    dataview1.setInt32(1, 4.5);
    document.write(dataview1.getInt32(1) + "<br>");

</script>
```

**输出:**

```
4
```

**代码#3:**
当没有数据要存储时，则返回零(0)。

## java 描述语言

```
<script>

    // Creating buffer with size in byte
    var buffer = new ArrayBuffer(20);

    // Creating a view
    var dataview1 = new DataView(buffer, 0, 10);

    // putting no data at slot 1
    dataview1.setInt32(1);
    document.write(dataview1.getInt32(1) + "<br>");

</script>
```

**输出:**

```
0
```

**支持的浏览器:**

*   谷歌 Chrome 9 及以上版本
*   边缘 12 及以上
*   Firefox 15 及以上版本
*   Internet Explorer 10 及以上版本
*   Opera 12.1 及以上
*   Safari 5.1 及以上版本