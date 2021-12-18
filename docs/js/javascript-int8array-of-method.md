# JavaScript Int8Array of()方法

> 原文:[https://www . geesforgeks . org/JavaScript-int 8 array-of-method/](https://www.geeksforgeeks.org/javascript-int8array-of-method/)

**Int8Array** 构造函数表示 8 位有符号整数的二进制补码数组。默认情况下，Int8Array 的内容被初始化为 0。()的 **Int8Array.of()方法用于从类似数组或可迭代的对象创建新的 **Int8Array** 。**

**语法:**

```
Int8Array.of(el0, el1, ...)
```

**参数:**这个方法接受元素的个数，基本上就是为其创建数组的元素。

**返回值:**这个方法返回一个新的 Int8Array 实例。

**例 1:** 在本例中，传递的值是通过方法转换为 **Int8** 的字符值。

## 超文本标记语言

```
<script> 

    // Create a Int8Array from a array
    // by creating the array from the
    // Int8Array.of() method
    let int8Arr = new Int8Array;
    int8Arr = Int8Array.of('1', '5', '2', '8', '14');

    // Print the result 
    console.log(int8Arr); 
</script>
```

**输出:**

```
[1, 5, 2, 8, 14]
```

**例 2:** 在本例中，传递的值是通过方法转换为 **Int8** 的整数值。49999 和 799 分别转换为 79 和 31。

## 超文本标记语言

```
<script> 

    // Create a Int8Array from a array
    // by creating the array from the
    // Int8Array.of() method
    let int8Arr = new Int8Array;

    // Accepts the int8 values
    int8Arr = Int8Array.of(49999, 5, 6, 799, 8); 

    // Print the result 
    console.log(int8Arr); 
</script>
```

**输出:**

```
[79, 5, 6, 31, 8]

```