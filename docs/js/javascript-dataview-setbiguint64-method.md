# JavaScript dataview . setbiguint64()方法

> 原文:[https://www . geesforgeks . org/JavaScript-data view-setbiguint64-method/](https://www.geeksforgeeks.org/javascript-dataview-setbiguint64-method/)

**setBigUint64()方法**用于存储从数据视图开始的特定字节偏移量处的无符号 64 位整数(无符号长整型)值。

**语法:**

```
dataview.setBigUint64(byteOffset, val [, littleEndian])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Byte Offset:** This parameter specifies the offset of reading data from the view, in bytes.
*   **val:** This parameter specifies the value to be set to BigUInt.
*   [T0】 little endian: 【T1] is an optional parameter. If true, it indicates whether 64-bit int is stored in small or large format. If set to false or undefined, the big end value is read.

**返回值:**此函数返回未定义。

**示例 1:** 在此示例中，偏移 0 处的值集为 1234。

## HTML

```
<script>
    var buffr = new ArrayBuffer(8);
    var dView = new DataView(buffr);
    dView.setBigUint64(0, 1234n);
    document.write(dView.getBigUint64(0));
</script>
```

**输出:**

```
1234

```

**示例 2:** 在此示例中，偏移 6 处的值集为 12345678。

## HTML

```
<script>
    // Creating an ArrayBuffer with a size in bytes
    const buffr = new ArrayBuffer(32);
    // Setting constant value
    const val = 12345678n;
    const dView = new DataView(buffr);
    dView.setBigUint64(6, val);
    document.write(dView.getBigUint64(6));
</script>
```

**输出:**

```
12345678

```