# 在 JavaScript 中不使用模运算符如何检查一个数是否为偶数？

> 原文:[https://www . geesforgeks . org/如何在不使用 javascript 中的模运算符的情况下检查数字是否为偶数/](https://www.geeksforgeeks.org/how-to-check-a-number-is-even-without-using-modulo-operator-in-javascript/)

在本文中，我们学习如何在不使用 [%](https://www.geeksforgeeks.org/modulo-operator-in-c-cpp-with-examples/) 或模运算符的情况下检查一个数是否为偶数。方法如下。

**1。通过使用按位*****&*****运算符:**

**说明:**

> 那么 2&1=0！(0)是真的，所以 2 是偶数
> 0 0 1 0
> &
> 0 0 0 1
> 0 0 0
> 3&1 = 1 那么！(1)是假的，所以 3 是奇数
> 0 0 1 1
> &
> 0 0 1
> 0 0 1

## 超文本标记语言

```
<script>
   function isEvenNumber(num) {
      if (!(num & 1)) {
         return `${num} is an even number`;
      } else {
         return `${num} is an odd number`;
      }
   }
   console.log(isEvenNumber(2));
   console.log(isEvenNumber(3));
</script>
```

**输出:**

```
2 is an even number
3 is an odd number
```

**2。通过将一个数字乘以二并除以二:**偶数不会丢失十进制值，因此比较将是*真*。在奇数的情况下，小数点值将丢失，比较将为*假*。

## 超文本标记语言

```
<script>
   function isEvenNumber(num) {
   if(Math.floor(num / 2) * 2 === num) {
         return `${num} is an even number`;
      } else {
         return `${num} is an odd number`;
      }
   }
   console.log(isEvenNumber(2));
   console.log(isEvenNumber(3));
</script>
```

**输出:**

```
2 is an even number
3 is an odd number
```

**3。通过使用正则表达式(JavaScript Regex):** 在这个方法中，我们检查最后一个数字。如果最后一个数字介于(0，2，4，6，8)之间，则该数字是偶数，否则该数字是奇数。

## 超文本标记语言

```
<script>
   function isEvenNumber(num) {
   if(/^\d*[02468]$/.test(num)) {
         return `${num} is an even number`;
      } else {
         return `${num} is an odd number`;
      }
   }
   console.log(isEvenNumber(2));
   console.log(isEvenNumber(3));
</script>
```

**输出:**

```
2 is an even number
3 is an odd number
```

**4。通过使用数字类的预定义方法:**我们使用数字类的 [isInteger()](https://www.geeksforgeeks.org/javascript-number-isinteger-function/) 方法来确定数字是否属于整数。如果数字不是整数，函数返回*假*，如果数字是整数，函数返回*真*。

```
2/2 =0  where 0 is an integer
3/2=1.5 where 1.5 is an integer
```

## 超文本标记语言

```
<script>
   function isEvenNumber(num) {
   if(Number.isInteger(num / 2)) {
         return `${num} is an even number`;
      } else {
         return `${num} is an odd number`;
      }
   }
   console.log(isEvenNumber(2));
   console.log(isEvenNumber(3));
</script>
```

**输出:**

```
2 is an even number
3 is an odd number
```

**5。通过使用条件循环:**我们从 2 中减去一个数，直到该数小于 2。然后我们要看剩下的数字是 1 还是 0。如果答案是 1，那么这个数就是奇数，否则这个数就是偶数。

## 超文本标记语言

```
<script>
   function isEvenNumber(num) {

      // Math.abs() is for negative number
      num = Math.abs(num);
      while (num >= 2) {
         num = num - 2;
      }
      if (num === 1) {
         return `${num} is an odd number`;
      } else {
         return `${num} is an even number`;
      }
   }
   console.log(isEvenNumber(2));
   console.log(isEvenNumber(3));
</script>
```

**输出:**

```
2 is an even number
3 is an odd number
```