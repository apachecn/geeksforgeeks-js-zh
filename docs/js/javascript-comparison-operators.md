# JavaScript 比较运算符

> 原文:[https://www . geesforgeks . org/JavaScript-比较-运算符/](https://www.geeksforgeeks.org/javascript-comparison-operators/)

在本文中，我们将了解各种比较运算符&它们在 Javascript 中的实现。**比较运算符**主要用于执行确定值之间相等或不同的逻辑运算。

[运算符](https://www.geeksforgeeks.org/javascript-operators/)用于对操作数执行特定的数学和逻辑计算。像 C、C++、Java、Python 和各种其他语言一样，JavaScript 也支持**比较**操作。**比较运算符**用于逻辑表达式中，以确定它们在变量或值上的相等或不同。

**示例:**下面是比较运算符的示例。

## java 描述语言

```
<script>
    function gfg() {
    let val1 = 5;

    // Equality Operators
    document.write(val1 == 5);
    document.write("<br>");

    // Relational Operators
    document.write(val1 > 0);
    }
    gfg();
</script>
```

**输出:**

```
true
true
```

JavaScript 支持多种比较运算符:

*   **等式运算符**
*   **关系运算符**

我们将通过示例依次讨论这两种运算符。

**等式运算符:**

**相等(==):** 此运算符用于比较两个操作数的相等性。如果相等，则条件为真，否则为假。

**语法:**

```
x == y
```

**示例 1:** 下面的示例说明了 JavaScript 中的 **(==)** 运算符。

## java 描述语言

```
<script>

    // Illustration of (==) operator
    let val1 = 5;
    let val2 = '5';

    // Checking of operands
    console.log(val1 == 5);
    console.log(val2 == 5);       
    console.log(val1 == val1);

    // Check against null and boolean value
    console.log(0 == false);  
    console.log(0 == null);
</script>
```

**输出:**

```
> true
> true
> true
> true
> false
```

**示例 2:** 本示例描述了比较 2 个对象值的等式运算符。

## java 描述语言

```
<script>

    // Illustration of (==) operator
    let obj1 = {'val1': 'value'};
    let obj2 = {'val2': 'value'};

    // Checking of operands
    console.log(obj1.val1 == 'value');       
    console.log(obj1 == obj2);
    console.log(obj1.val1 == obj2.val2);

    // Check against undefined
    console.log(0 == undefined);  
    console.log(null == undefined);
</script>
```

**输出:**

```
> true
> false
> true
> false
> true
```

**我****nequality****(！=):** 这个运算符用来比较两个操作数的不等式。如果相等，则条件为假，否则为真。

**语法:**

```
x != y
```

**例 1:** 下面的例子说明了 **(！=)** 在 JavaScript 中操作符。

## java 描述语言

```
<script>

    // Illustration of (!=) operator
    let val1 = 5;
    let val2 = '5';

    // Checking of operands
    console.log(val1 != 6);
    console.log(val2 != '5');       
    console.log(val1 != val1);

    // Check against null and boolean value
    console.log(0 != false);  
    console.log(0 != null);
</script>
```

**输出:**

```
> true
> false
> false
> false
> true
```

**示例 2:** 本示例描述了比较两个值的不等式运算符。

## java 描述语言

```
<script>

    // Illustration of (!=) operator
    let obj1 = {'val1': 'value'};
    let obj2 = {'val2': 'value'};

    // Checking of operands
    console.log(obj1.val1 != 'value');       
    console.log(obj1 != obj2);
    console.log(obj1.val1 != obj2.val2);

    // Check against undefined
    console.log(0 != undefined);  
    console.log(null != undefined);
</script>
```

**输出:**

```
> false
> true
> false
> true
> false
```

**严格** **等式****(= =):**这个运算符用来 c ompare 两个操作数的等式同类型。如果值和类型相等，则条件为真，否则为假。

**语法:**

```
x === y
```

**示例 1:** 下面的示例说明了 JavaScript 中的**(= =)**运算符。

## java 描述语言

```
<script>

    // Illustration of (===) operator
    let val1 = 5;
    let val2 = '5';

    // Checking of operands
    console.log(val1 === 6);
    console.log(val2 === '5');       
    console.log(val1 === val1);

    // Check against null and boolean value
    console.log(0 === false);  
    console.log(0 === null);
</script>
```

**输出:**

```
> false
> true
> true
> false
> false
```

**示例 2:** 本示例描述了比较 2 个值的严格等式运算符。

## java 描述语言

```
<script>

    // Illustration of (===) operator
    let obj1 = {'val1': 'value'};
    let obj2 = {'val2': 'value'};

    // Checking of operands
    console.log(obj1.val1 === 'value');       
    console.log(obj1 === obj2);
    console.log(obj1.val1 === obj2.val2);

    // Check against undefined
    console.log(0 === undefined);  
    console.log(null === undefined);
</script>
```

**输出:**

```
> true
> false
> true
> false
> false
```

它们之间的显著差异请参考[= = = ' vs ' = = '比较运算符](https://www.geeksforgeeks.org/javascript-vs-comparision-operator/)一文。

**严于** **平等** **(！==):** 这个运算符用来 c 用类型来表示两个操作数的不等式。如果值和类型不相等，则条件为真，否则为假。

**语法:**

```
x !== y
```

**例 1:** 下面的例子说明了 **(！==)** 在 JavaScript 中操作符。

## jscript

```
<script>
 // Illustration of (!==) operator
 let val1 = 5;
 let val2 = '5';

 // Checking of operands
 console.log(val1 !== 6);
 console.log(val2 !== '5');       
 console.log(val1 !== val1);

 // Check against null and boolean value
 console.log(0 !== false);  
 console.log(0 !== null);
</script>
```

**输出:**

```
> true
> false
> false
> true
> true
```

**示例 2:** 此示例描述了比较 2 个值的严格不等式运算符。

## java 描述语言

```
<script>

    // Illustration of (!==) operator
    let obj1 = {'val1': 'value'};
    let obj2 = {'val2': 'value'};

    // Checking of operands
    console.log(obj1.val1 !== 'value');       
    console.log(obj1 !== obj2);
    console.log(obj1.val1 !== obj2.val2);

    // Check against undefined
    console.log(0 !== undefined);  
    console.log(null !== undefined);
</script>
```

**输出:**

```
> false
> true
> false
> true
> true
```

**关系运算符:**

**G** **比运算符** **( > ):** 这个运算符是用来到检查的左侧的值是否大于右侧的值。如果值更大，则条件为真，否则为假。

**语法:**

```
x > y
```

**例 1:** 下面的例子说明了 JavaScript 中的 **( > )** 运算符。

## java 描述语言

```
<script>

    // Illustration of (>) operator
    let val1 = 5;
    let val2 = "5";

    // Checking of operands
    console.log(val1 > 0);
    console.log(val2 > "10");       
    console.log(val1 > "10");
    console.log(val2 > 0);
</script>
```

**输出:**

```
> true
> true
> false
> true
```

**示例 2:** 本示例描述了比较 2 个值的大于运算符。

## java 描述语言

```
<script>

    // Illustration of (>) operator
    let obj1 = {'val1': 1};
    let obj2 = {'val2': 3};

    // Checking of operands
    console.log(obj1.val1 > 0);       
    console.log(obj1 > obj2);
    console.log(obj1.val1 > obj2.val2);
    console.log(obj2 > obj1);
    console.log(obj2.val2 > obj1.val1);
</script>
```

**输出:**

```
> true
> false
> false
> false
> true
```

**G** **大于或等于运算符** **( > =):** 该运算符用于检查左侧操作数是否大于或等于右侧操作数。如果值为 g 大于或等于 ，则条件为真，否则为假。

**语法:**

```
x >= y
```

**例 1:** 下面的例子说明了 JavaScript 中的 **( > =)** 运算符。

## java 描述语言

```
<script>

 // Illustration of (>=) operator
 let val1 = 5;
 let val2 = "5";

 // Checking of operands
 console.log(val1 >= 5);
 console.log(val2 >= "15");       
 console.log(val1 >= "5");
 console.log(val2 >= 15);
</script>
```

**输出:**

```
> true
> true
> true
> false
```

**示例 2:** 本示例描述了比较两个值的大于或等于运算符。

## java 描述语言

```
<script>

    // Illustration of (>=) operator
    let obj1 = {'val1': 1};
    let obj2 = {'val2': 3};

    // Checking of operands
    console.log(obj1.val1 >= 0);       
    console.log(obj1 >= obj2);
    console.log(obj1.val1 >= obj2.val2);
    console.log(obj2 >= obj1);
    console.log(obj2.val2 >= obj1.val1);
</script>
```

**输出:**

```
> true
> true
> false
> true
> true
```

**L** **ess 比运算符** **( < ):** 此运算符用于检查左侧值是否小于右侧值。如果是，则条件为真，否则为假。

**语法:**

```
x < y
```

**例 1:** 下面的例子说明了 JavaScript 中的 **( < )** 运算符。

## java 描述语言

```
<script>

 // Illustration of (<) operator
 let val1 = 5;
 let val2 = "5";

 // Checking of operands
 console.log(val1 < 15);
 console.log(val2 < "0");       
 console.log(val1 < "0");
 console.log(val2 < 15);
</script>
```

**输出:**

```
> true
> false
> false
> true
```

**示例 2:** 本示例描述了比较两个值的小于运算符。

## java 描述语言

```
<script>

    // Illustration of (<) operator
    let obj1 = {'val1': 1};
    let obj2 = {'val2': 3};

    // Checking of operands
    console.log(obj1.val1 < 10);       
    console.log(obj1 < obj2);
    console.log(obj1.val1 < obj2.val2);
    console.log(obj2 < obj1);
    console.log(obj2.val2 < obj1.val1);
</script>
```

**输出:**

```
> true
> false
> true
> false
> false
```

**L** **ess 小于或等于运算符** **( < =):** 该运算符用于检查  左侧操作数值是否小于或等于右侧操作数值。如果是 ，则条件为真，否则为假。

**语法:**

```
x <= y
```

**例 1:** 下面的例子说明了 JavaScript 中的 **( < =)** 运算符。

## java 描述语言

```
<script>

    // Illustration of (<=) operator
    let val1 = 5;
    let val2 = "5";

    // Checking of operands
    console.log(val1 <= 15);
    console.log(val2 <= "0");       
    console.log(val1 <= "0");
    console.log(val2 <= 15);
</script>
```

**输出:**

```
> true
> false
> false
> true
```

**示例 2:** 本示例描述了小于或等于运算符来比较 2 个值。

## java 描述语言

```
<script>

    // Illustration of (<=) operator
    let obj1 = {'val1': 1};
    let obj2 = {'val2': 3};

    // Checking of operands
    console.log(obj1.val1 <= 10);       
    console.log(obj1 <= obj2);
    console.log(obj1.val1 <= obj2.val2);
    console.log(obj2 <= obj1);
    console.log(obj2.val2 <= obj1.val1);
</script>
```

**输出:**

```
> true
> true
> true
> true
> false
```

**支持的浏览器:**所有 **JavaScript 比较运算符**支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   歌剧
*   旅行队
*   微软边缘
*   微软公司出品的 web 浏览器