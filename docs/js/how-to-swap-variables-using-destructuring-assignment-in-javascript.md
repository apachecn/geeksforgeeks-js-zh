# 如何在 JavaScript 中使用析构赋值来交换变量？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 中的析构赋值来交换变量/](https://www.geeksforgeeks.org/how-to-swap-variables-using-destructuring-assignment-in-javascript/)

**[【解构赋值】](https://www.geeksforgeeks.org/destructuring-assignment-in-javascript/)** 是 [EcmaScript2015](https://www.geeksforgeeks.org/introduction-to-es6/) 中引入的一个特性，它允许您将数组的内容、对象的属性提取到不同的变量中，而无需编写重复的代码。

**示例 1:** 在此示例中，我们声明了两个未赋值的变量 *a* 和 *b* ，以及一个包含两个字符串“第一”和“第二”的数组。在第 5 行，我们使用析构赋值将数组的值分别赋给和 b。

## Javascript

```
<script>
  let a;
  let b;
  let array = ["First", "Second"];

  [a, b] = array;
  console.log("a:", a);
  console.log("b:", b);
</script>
```

**输出:**

```
a: First 
b: Second
```

如您所见，变量 *a* 被赋值为字符串“第一”，变量 *b* 被赋值为字符串“第二”。

**示例 2:** 这里我们声明了两个变量 *a* 和 *b* 分别具有值“第一”和“第二”。在下一行中，我们使用析构赋值来交换变量。

## Javascript

```
<script>
  let a = "First";
  let b = "Second";
  [a, b] = [b, a];

  console.log("a:", a);
  console.log("b:", b);
</script>
```

**输出:**

```
a: Second
b: First
```