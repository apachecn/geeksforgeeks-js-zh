# JavaScript dataView.setUint8()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-data view-setuint 8/

下面是 **dataView.setUint8()** 方法的例子。

**例:**

## java 描述语言

```
<script>
var buffer = new ArrayBuffer(20);

var dataview1 = new DataView(buffer, 0, 10);

dataview1.setUint8(1, 12);
document.write(dataview1.getUint8(1));
</script>
```

**输出:**

```
12
```

**dataView.setUint8()** 是 dataView 中的一个内置函数，用于在指定位置存储无符号 8 位整数，即从 dataView 开始的字节偏移量。
**语法:**

```
dataView.setUint8(byteOffset)
```

**参数:**它有一个字节偏移的参数 byteOffset，它表示从视图开始读取数据。
**返回值:**这个函数不返回任何东西。
**例 1:**

```
Input: dataview1.setUint8(1, 56);
Output: 56
```

**例 2:**

```
Input: dataview1.setUint8(1, Math.PI);
Output: 3
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
   dataview1.setUint8(1, 56);
   document.write(dataview1.getUint8(1));

</script>
```

**输出:**

```
56
```

**代码#2:**
该函数不接受浮点值，这就是它将浮点值转换为整数值的原因。从下面程序的输出可以看出，它给出的输出应该是 3.14(PI 的值)，但是这个函数将这个值转换为 3。

## java 描述语言

```
<script>

   // Creating buffer with size in byte
   var buffer = new ArrayBuffer(20);

   // Creating a view with slot from o to 10
   var dataview1 = new DataView(buffer, 0, 10);

   // put the value of PI at slot 1
   dataview1.setUint8(1, Math.PI);
   document.write(dataview1.getUint8(1) + "<br>");

</script>
```

**输出:**

```
3
```

**代码#3:**
当没有任何数据用于存储时，它给出的输出为零(0)。

## java 描述语言

```
<script>

   // Creating buffer with size in byte
   var buffer = new ArrayBuffer(20);

   // Creating a view
   var dataview1 = new DataView(buffer, 0, 10);

   // putting no data at slot 1
   dataview1.setUint8(1);
   document.write(dataview1.getUint8(1) + "<br>");

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