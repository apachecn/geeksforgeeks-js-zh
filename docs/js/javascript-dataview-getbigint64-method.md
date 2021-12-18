# JavaScript dataview . getbigint 64()方法

> 原文:[https://www . geesforgeks . org/JavaScript-data view-getbigint 64-method/](https://www.geeksforgeeks.org/javascript-dataview-getbigint64-method/)

下面是 **dataView.setInt8()** 方法的例子。

*   **例:**

    ```
    <script>  
       var buffr = new ArrayBuffer(12);  

       var dataview = new DataView(buffr);   
       document.write(dataview.getBigInt64(0)); 
    </script>
    ```

*   **输出:**

    ```
    0
    ```

这个 getBigInt64()方法用于从数据视图开始的特定字节偏移量处获取有符号的 64 位整数(长整型)。

**语法:**

```
dataview.getBigInt64(byteOffset [, littleEndian])
```

**参数:**

*   **byteofset:**此参数指定从视图开始读取数据的偏移量，以字节为单位。
*   **littleEndian:** 这是可选参数。如果为真，则指示 64 位 int 是以小端格式还是大端格式存储。如果设置为 false 或未定义，则读取大端值。

**返回值:**返回一个 BigInt 值。

**抛出错误:**如果字节偏移量超出了视图的结尾，则抛出**范围错误**。

**例 1:** 在本例中，传递的偏移量为 0，因此打印的值为 0，因为没有设置任何内容。

```
<script> 
   // Creating buffer with size in byte 
   var buffr = new ArrayBuffer(8); 

   // Creating a view 
   var dataview = new DataView(buffr);  
   document.write(dataview.getBigInt64(0));
</script>
```

**输出:**

```
0
```

**例 2:** 在本例中，传递的偏移量为 3，因此打印的值为 10000，因为它是之前设置的。

```
<script>
    // create an ArrayBuffer with a size in bytes
    const buffr = new ArrayBuffer(16);
    // constant value to set
    const max = 10000n;
    const view = new DataView(buffr);
    view.setBigInt64(3, max);
    document.write(view.getBigInt64(3));
</script>
```

**输出:**

```
10000
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧