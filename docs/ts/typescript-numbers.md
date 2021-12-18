# 打字稿号

> 原文:[https://www.geeksforgeeks.org/typescript-numbers/](https://www.geeksforgeeks.org/typescript-numbers/)

TypeScript 类似于 JavaScript，它支持数值作为 Number 对象。typescript 中的数字既用作整数，也用作浮点值。number 类充当包装器，并像处理对象一样处理数字文本。

**语法:**

```
var var_name = new Number(value)
```

**属性:**

*   **MAX_VALUE:** 它在 JavaScript 中有最大可能值 1.7976931348623157E+308。
*   **MIN_VALUE:** 它在 JavaScript 中有最小可能值 5E-324。
*   **NaN:** 该属性的 Equal 值不是数字。
*   **NEGATIVE_INFINITY:** 该值小于 MIN_VALUE。
*   **正数 _ 无穷大:**该值大于最大值。
*   **原型:**该属性用于为 Number 对象分配新的属性和方法。
*   **构造函数:**该属性将返回创建该对象实例的函数

**示例:**

```
console.log(" Number Properties in TypeScript: "); 
console.log("Maximum value of a number variable has : " 
                                   + Number.MAX_VALUE); 
console.log("The least value of a number variable has: " 
                                    + Number.MIN_VALUE); 
console.log("Value of Negative Infinity: " 
                             + Number.NEGATIVE_INFINITY); 
console.log("Value of Negative Infinity:" 
                             + Number.POSITIVE_INFINITY);
```

**输出:**

```
Number Properties in TypeScript:  
Maximum value of a number variable has: 1.7976931348623157e+308 
The least value of a number variable has: 5e-324 
Value of Negative Infinity: -Infinity 
Value of Negative Infinity:Infinity
```

**NaN 示例:**

```
var day = 0 
if( day<=0 || v >7) { 
   day = Number.NaN 
   console.log("Day is "+ day) 
} else { 
   console.log("Value Accepted..") 
}
```

**输出:**

```
Month is NaN
```

**方法:**

*   **toExponential():** 此方法将返回一个数字，以指数记数法显示。
*   **toFixed():** 这个方法会用特定的位数来稳定小数点右边的数字。
*   **toLocaleString():** 此方法用于将数字转换为数字的本地特定表示。
*   **toPrecision():** 它将定义小数点左右的总位数来显示一个数字。当精度为负时，也会显示错误。
*   **toString():** 用于返回指定基数内数字的字符串表示形式。
*   **valueOf():** 此方法将返回数字的原始值。

**例 1:**

```
// The toExponential() 
var num1 = 2525.30 
var val = num1.toExponential(); 
console.log(val)
```

**输出:**

```
2.5253e+3
```

**例 2:**

```
// The toFixed()
var num3 = 237.134 
console.log("num3.toFixed() is "+num3.toFixed()) 
console.log("num3.toFixed(2) is "+num3.toFixed(3)) 
console.log("num3.toFixed(6) is "+num3.toFixed(5))
```

**输出:**

```
num3.toFixed() is 237 
num3.toFixed(2) is 237.134 
num3.toFixed(6) is 237.13400
```

**例 3:**

```
// The toLocaleString()
var num = new Number( 237.1346); 
console.log( num.toLocaleString());
```

**输出:**

```
237.1346
```

**例 4:**

```
// The toPrecision()
var num = new Number(5.7645326); 
console.log(num.toPrecision()); 
console.log(num.toPrecision(1)); 
console.log(num.toPrecision(2));
```

**输出:**

```
5.7645326 
5 
5.7
```

**例 5:**

```
// The toString()
var num = new Number(10); 
console.log(num.toString()); 
console.log(num.toString(2)); 
console.log(num.toString(8));
```

**输出:**

```
10 
1010 
12
```

**例 6:**

```
// The valueOf()
var num = new Number(20); 
console.log(num.valueOf());
```

**输出:**

```
20
```