# JavaScript dataview . setbigint 64()方法

> 原文:[https://www . geesforgeks . org/JavaScript-data view-setbigint 64-method/](https://www.geeksforgeeks.org/javascript-dataview-setbigint64-method/)

这个 **setBigInt64()方法**用于存储从数据视图开始的特定字节偏移量处的有符号 64 位整数(长整型)值。

**语法:**

```
dataview.setBigInt64(byteOffset, val [, littleEndian])
```

**参数:**

*   **Byte Offset:** This parameter specifies the offset of reading data from the view, in bytes.
*   **Val:** This parameter specifies the value to be set to BigInt.
*   [T0】 little endian: 【T1] This is an optional parameter. If true, it indicates whether 64-bit int is stored in small or large format. If set to false or undefined, the big end value is read.

**返回值:**

这个函数不返回任何东西。

**示例 1:** 在此示例中，偏移 0 处的值设置为 7。

```
<script>
    var buffr = new ArrayBuffer(8);
    var dView = new DataView(buffr);
    dView.setBigInt64(0, 7n);
    document.write(dView.getBigInt64(0));
</script>
```

**输出:**

```
7
```

**示例 2:** 在此示例中，偏移 4 处的值集为 789。

```
<script>
    // create an ArrayBuffer with a size in bytes
    const buffr = new ArrayBuffer(16);
    // constant value to set
    const val = 789n;
    const dView = new DataView(buffr);
    dView.setBigInt64(4, val);
    document.write(dView.getBigInt64(4));
</script>
```

**输出:**

```
789
```