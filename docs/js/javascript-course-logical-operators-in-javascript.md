# JavaScript 课程| JavaScript 中的逻辑运算符

> 原文:[https://www . geesforgeks . org/JavaScript-课程-逻辑-运算符-in-javascript/](https://www.geeksforgeeks.org/javascript-course-logical-operators-in-javascript/)

**上一篇:** [JavaScript 课程|与用户交互](https://www.geeksforgeeks.org/javascript-course-interaction-with-user/)
JavaScript 中有三个逻辑运算符:

*   **！(不是)**
*   **& & (AND)**
*   **||(或)**

**！(非)**
它反转操作数(或条件)的布尔结果。

```
result = !value;
```

以下运算符只接受一个参数，并执行以下操作:

*   将操作数转换为布尔类型，即*真/假*
*   返回翻转的值

**示例:**

## java 描述语言

```
<script>
// !(NOT) operator
let geek = 1;
alert(!geek);
</script>
```

**输出:**

```
false
```

运算符将值“1”转换为布尔值，结果是“真”，然后在翻转(反转)该值后，这就是为什么当我们最终提醒该值时，我们得到“假”。

**&&(AND)**
&&运算符接受多个参数，它主要执行以下操作:

*   从左到右计算操作数
*   对于每个操作数，它将首先将其转换为布尔值。如果结果为假，则停止并返回该操作数的原始值。
*   否则，如果一切都是真实的，它将返回最后真实的价值。

```
result = a && b; // can have multiple arguments.
```

**示例:**

## java 描述语言

```
<script>
// &&(AND) operator
alert( 0 && 1 ); // 0
alert( 1 && 3 ); // 3
alert( null && true ); // null
alert( 1 && 2 && 3 && 4); // 4
</script>
```

**输出:**

```
0
3
null 
4
```

**| |(OR)**
OR 运算符与 AND 运算符有些相反。它执行以下操作:

*   从左到右计算操作数。
*   对于每个操作数，它将首先将其转换为布尔值。如果结果为真，则停止并返回该操作数的原始值。
*   否则，如果所有值都是假的，它将返回最后一个值。

```
result = a || b;
```

**示例:**

## java 描述语言

```
<script>
// ||(OR) Operator
alert( 0 || 1 ); // 1
alert( 1 || 3 ); // 1
alert( null || true ); // true
alert( -1 || -2 || -3 || -4); // -1
</script>
```

**输出:**

```
1
1
true
-1
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软边缘
*   火狐浏览器
*   歌剧
*   旅行队

**下一篇:** [JavaScript 教程| JavaScript 中的条件运算符](https://www.geeksforgeeks.org/javascript-course-conditional-operator-in-javascript/)