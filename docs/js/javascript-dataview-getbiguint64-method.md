# JavaScript dataview . getbiguint64()方法

> 原文:[https://www . geesforgeks . org/JavaScript-data view-getbiguint64-method/](https://www.geeksforgeeks.org/javascript-dataview-getbiguint64-method/)

**getBigUint64()方法**用于从数据视图开始的特定字节偏移量处获取无符号 64 位整数(无符号长整型)。

**语法:**

```
dataview.getBigUint64(byteOffset [, littleEndian])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **byteofset:**此参数指定从视图开始读取数据的偏移量，以字节为单位。
*   **littleEndian:** 为可选参数。如果为真，则表明 64 位 int 是以小端还是大端格式存储的。如果设置为 false 或未定义，则读取大端值。

**返回值:**返回一个 BigInt 值。

**例 1:** 在本例中，传递的偏移量为 0，因此打印的值为 0，因为没有设置该值。

## 超文本标记语言

```
<script> 
   // Creating buffer with size in byte 
   var buffr = new ArrayBuffer(16); 

   // Creating a view 
   var dView = new DataView(buffr);

   // Getting the value
   document.write(dView.getBigUint64(0));
</script>
```

**输出:**

```
0

```

**例 2:** 在本例中，传递的偏移量为 4，因此打印的值为 1234，因为它是之前设置的。

## 超文本标记语言

```
<script>
    // Create an ArrayBuffer with a size in bytes
    const buffr = new ArrayBuffer(16);

    // A value to set
    const val = 1234n;
    const view = new DataView(buffr);

    view.setBigUint64(4, val);

    // Getting the value
    document.write(view.getBigUint64(4));
</script>
```

**输出:**

```
1234

```