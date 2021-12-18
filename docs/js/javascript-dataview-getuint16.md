# JavaScript dataview . getuint 16()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-data view-getuint 16/

下面是 **dataView.getUint16()()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
   var buffer = new ArrayBuffer(20);

   var dataview1 = new DataView(buffer, 0, 10);

   dataview1.setUint16(1, 12);
  document.write(dataview1.getUint16(1));
</script>
```

*   **输出:**

```
12
```

**dataView.getUint16()** 是 dataView 中的一个内置函数，用于在指定位置，即从 dataView 开始的字节偏移量处获取一个无符号的 16 位整数。
**语法:**

```
dataView.getUint16(byteOffset)
```

**参数:**它有一个字节偏移的参数 byteOffset，它表示从视图开始读取数据。
**返回值:**返回无符号 16 位整数。
**例 1:**

```
Input: dataview1.setUint16(1, 56); 
       document.write(dataview1.getUint16(1)); 
Output: 56
```

**例 2:**

```
Input: dataview1.setUint16(1, Math.PI); 
       document.write(dataview1.getUint16(1)); 
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
   dataview1.setUint16(1, 56);
  document.write(dataview1.getUint16(1) + "<br>");

</script>
```

**输出:**

```
56
```

**代码#2:**
该功能将 PI 的浮点值从 3.14 转换为 3

## java 描述语言

```
<script>

   // Creating buffer with size in byte
   var buffer = new ArrayBuffer(20);

   // Creating a view with slot from o to 10
   var dataview1 = new DataView(buffer, 0, 10);

   // put the value of PI at slot 1
   dataview1.setUint16(1, Math.PI);
   document.write(dataview1.getUint16(1) + "<br>");

</script>
```

**输出:**

```
3
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
   dataview1.setUint16(1);
   document.write(dataview1.getUint16(1) + "<br>");

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