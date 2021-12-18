# JavaScript dataview . setfloat 64()方法

> 哎哎哎::1230【https://www . geeksforgeeks . org/JavaScript-dataview-set float 64/

下面是 **dataView.setFloat64()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
var buffer = new ArrayBuffer(20);

var dataview1 = new DataView(buffer, 0, 10);

dataview1.setFloat64(1, 12.22);
document.write(dataview1.getFloat64(1));
</script>
```

*   **输出:**

```
12.22
```

**dataView.setFloat64()** 是 dataView 中的一个内置函数，用于将带符号的 64 位浮点值存储在指定位置，即从 dataView 开始的字节偏移量处。
**语法:**

```
dataView.setFloat64(byteOffset)
```

**参数:**它有一个字节偏移的参数 byteOffset，即从视图开始读取数据。
**返回值:**这个函数不返回任何东西。
**例 1:**

```
Input: dataview1.setFloat64(1, 56.24);
Output: 56.24
```

**例 2:**

```
Input: dataview1.setFloat64(1, Math.PI); 
Output: 3.141592653589793
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

   // put the data 56.24 at slot 1
   dataview1.setFloat64(1, 56.24);
   document.write(dataview1.getFloat64(1));

</script>
```

**输出:**

```
56.24
```

**代码#2:**
下面的代码使用数学设置圆周率的值。并将输出作为 PI 的值给出。

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
3.141592653589793
```

**代码#3:**
当没有要存储的数据时，它给出的输出是 NaN，即不是一个数字。

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