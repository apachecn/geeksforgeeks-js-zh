# 类型脚本|数组连接()方法

> 原文:[https://www.geeksforgeeks.org/typescript-array-join-method/](https://www.geeksforgeeks.org/typescript-array-join-method/)

**Array.join()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于将数组的所有元素连接成一个字符串。
**语法:**

```
array.join(separator)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **分隔符:**这个参数是用来分隔数组中每个元素的字符串。

**返回值:**该方法在连接所有数组元素后返回字符串。
以下示例说明了 TypeScript 中的**数组连接()**方法。

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of join() method 
    var str = arr.join(", ")

    // printing element
    console.log("String : " + str);
</script>
```

**输出:**

```
String : 11, 89, 23, 7, 98

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 'a','b','c','a','e' ]; 

    // use of join() method 
    var val = arr.join(" ")
    var val1 = arr.join(" + ")

    // printing element
    console.log(val);
    console.log(val1);
</script>
```

**输出:**

```
a b c a e
a + b + c + a + e

```