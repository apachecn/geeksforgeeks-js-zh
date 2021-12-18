# JavaScript uint 8 clampedarray . of()方法

> 原文:[https://www . geesforgeks . org/JavaScript-uint 8 clampedarray-of-method/](https://www.geeksforgeeks.org/javascript-uint8clampedarray-of-method/)

**Uint8ClampedArray** 数组是一个 8 位无符号整数数组，被箝位在 0-255 之间。如果传递的值小于 0 或大于 255，则将改为设置该值。如果指定了非整数，则将设置最接近的整数。

**方法通过可变数量的参数创建一个新的类型化数组。**

**语法:**

```
Uint8ClampedArray.of(el0, el1, el2, ..., eln)

```

**参数:**

*   **n-elements:** 这个方法接受元素的个数，基本上就是为其创建数组的元素。

**返回值:**这个方法返回一个新的 Uint8ClampedArray 实例。

**示例 1:** 在本示例中，传递的值是通过方法转换为 Uint8Clamped 的字符值。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <script> 
        // Creating a Uint8ClampedArray from
        // an array by creating the array from
        // the Uint8ClampedArray.of() method
        let uint8CArr = new Uint8ClampedArray;
        uint8CArr = Uint8ClampedArray.of(
            '40', '51', '56', '18', '24');

        // Printing the result 
        console.log(uint8CArr); 
    </script>
</body>

</html>
```

**输出:**

```
Uint8ClampedArray(5) [40, 51, 56, 18, 24]
```

**示例 2:** 在此示例中，传递的值是由方法转换为 Uint8Clamped 的 int 值。-9999 和 799 分别转换为 0 和 255。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <script> 
        // Creating a Uint8ClampedArray from
        // an array by creating the array from
        // the Uint8ClampedArray.of() method
        let uint8CArr = new Uint8ClampedArray;

        // Accepts the uint8C values
        uint8CArr = Uint8ClampedArray.of(
            -9999, 50, 7, 799, 8); 

        // Print the result 
        console.log(uint8CArr); 
    </script>
</body>

</html>
```

**输出:**

```
 Uint8ClampedArray(5) [0, 50, 7, 255, 8]

```