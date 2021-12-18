# JavaScript 号原型属性

> 原文:[https://www . geesforgeks . org/JavaScript-number-prototype-property/](https://www.geeksforgeeks.org/javascript-number-prototype-property/)

**Number**JavaScript 中的对象用于操纵数字，无论是负数还是正数。JavaScript 数字类型表示双(小数值)类型的数字。像 98 这样的数字文字不是整数值，而是*浮点值*。它保持小数点后 17 位的精度。 **1.8 * 10^308** 是它能容纳的最大值，任何超过这个值的数字都被一个称为*无穷大*的常数所代替。

**Number.prototype** 指的是 **Number()** 对象，而不是单个 Number 对象。prototype 属性将以下实例方法添加到 number 对象中。

1.  **Number.prototype.toPrecision(precision_value):** It returns a string that represents a number to stated precision in exponential notation or fixed-point notation. The *precision_value* parameter specifies the number of digits in which the number need to be represented. The value of the parameter ranges from *0 to 20*, and if it is not in the given range, it produces an exception known as *RangeError*.

    **示例:**

    ```
    let num1 = 64.67890
    let num2 = 0.000123
    console.log(num1.toPrecision())    
    console.log(num1.toPrecision(3))  
    console.log(num1.toPrecision(1))  
    console.log(num2.toPrecision())    
    console.log(num2.toPrecision(3))  
    console.log(num2.toPrecision(1))  
    console.log((100000.02).toPrecision(4))
    ```

    **输出:**

    ```
    "64.6789"
    "64.7"
    "6e+1"
    "0.000123"
    "0.000123"
    "0.0001"
    "1.000e+5"

    ```

    ## java 描述语言

    ```
    function test(x) {
      return Number.parseFloat(x).toPrecision(5);
    }
    console.log(test(4532.567));
    console.log(test(0.00065));
    console.log(test('4.44e+5'));
    console.log(test('geeksforgeeks'));
    ```

    **输出:**

    ```
    "4532.6"
    "0.00065000"
    "4.4400e+5"
    "NaN"

    ```

2.  **number . prototype . value of():**返回指定对象的值。这个方法由 JavaScript 内部调用。

    **示例:**

    ```
    let num1 = new Number(105)
    console.log(num1)
    console.log(typeof num1)  
    let num2 = num1.valueOf()
    console.log(num2)            
    console.log(typeof num2)
    ```

    **输出:**

    ```
    105
    "object"
    105
    "number"

    ```

    **示例:**

    ## java 描述语言

    ```
    let num1 = new Number(100)
    console.log(num1)
    console.log(typeof num1)  
    let num2 = num1.valueOf()
    console.log(num2)            
    console.log(typeof num2)    
    ```