# 如何用 JavaScript 生成给定范围内的随机数？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 生成给定范围内的随机数/](https://www.geeksforgeeks.org/how-to-generate-random-number-in-given-range-using-javascript/)

一个过程产生的数字，其结果是不可预测的，称为随机数。在 JavaScript 中，这可以通过使用 Math.random()函数来实现。本文描述了如何使用 JavaScript 生成随机数。

**方法 1:使用 Math.random()函数:**math . random()函数用于返回范围在[0，1]，0(包含)和 1(不包含)之间的浮点伪随机数。然后，可以根据所需的范围对该随机数进行缩放。

**语法:**

```
Math.random();
```

**示例 1:** 本示例生成一个介于 1(最小值)和 5(最大值)之间的整数随机数。

```
<script> 

// Function to generate random number 
function randomNumber(min, max) { 
    return Math.random() * (max - min) + min;
} 

document.write("Random Number between 1 and 5: ") 

// Function call
document.write( randomNumber(1, 5) ); 
</script>                                  
```

**输出:**

```
Random Number between 1 and 5: 1.0573617826058959
```

**方法 2:使用 Math.floor()函数:**JavaScript 中的 Math.floor()函数用于将作为参数传递的数字向下舍入到最接近的整数，即向较小的值舍入。

**语法:**

```
Math.floor(value)
```

**示例 2:** 本示例生成 1(最小值)到 100(最大值)之间的随机整数。

```
<script> 

// Function to generate random number 
function randomNumber(min, max) { 
    return Math.floor(Math.random() * (max - min) + min);
} 

document.write("Random Number between 1 and 100: ") 

// Function call
document.write( randomNumber(1, 100) ); 
</script>                                     
```

**输出:**

```
Random Number between 1 and 100: 87
```

**示例 3:** 本示例生成 1(分)到 10(最大)之间的随机整数，包括 1 和 10。

```
<script> 

// Function to generate random number 
function randomNumber(min, max) { 
    min = Math.ceil(min);
    max = Math.floor(max);
    return Math.floor(Math.random() * (max - min + 1)) + min;
} 

document.write("Random Number between 1 and 10: ") 

// Function call
document.write( randomNumber(1, 10) ); 
</script>                                
```

**输出:**

```
Random Number between 1 and 10: 3
```