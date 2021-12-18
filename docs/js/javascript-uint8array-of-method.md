# JavaScript Uint8Array.of()方法

> 原文:[https://www . geesforgeks . org/JavaScript-uint 8 数组方法/](https://www.geeksforgeeks.org/javascript-uint8array-of-method/)

**Uint8Array** 数组表示 8 位无符号整数的数组。这些值由 0 初始化。数组中的元素可以由对象的方法引用，也可以使用标准语法(通过括号表示法)引用。

**uint 8 array . of()**方法根据可变数量的参数创建一个新的类型化数组。

**语法:**

```
Uint8Array.of(el0, el1, el2, .., eln)

```

**参数:**

*   **n-elements:** 这个方法接受元素的个数，基本上就是要为其创建数组的元素。

**返回值:**这个方法返回一个新的 Uint8Array 实例。

**示例 1:** 在本示例中，传递的值是通过方法转换为 Uint8 的字符值。

## Java Script 语言

```
<script> 
    // Creating a Uint8Array from a array by  
    // Creating the array from the Uint8Array.of() method
    let uint8Arr = new Uint8Array;
    uint8Arr = Uint8Array.of('41', '51', '56', '8', '24');

    // Printing the result 
    console.log(uint8Arr); 
</script>
```

**输出:**

```
Uint8Array(5) [41, 51, 56, 8, 24]
```

**示例 2:** 在此示例中，传递的值是通过方法转换为 Uint8 的 int 值。-49999 和 799 分别转换为 177 和 31。

## Java Script 语言

```
<script> 

    // Create a Uint8Array from a array by  
    // Creating the array from the Uint8Array.of() method
    let uint8Arr = new Uint8Array;

    // Accepts the uint8 values
    uint8Arr = Uint8Array.of(-49999, 5, 7, 799, 8); 

    // Print the result 
    console.log(uint8Arr); 
</script>
```

**输出:**

```
Uint8Array(5) [177, 5, 7, 31, 8]
```