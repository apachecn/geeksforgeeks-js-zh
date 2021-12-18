# 替代 JavaScript 中的多个或运算符

> 原文:[https://www . geesforgeks . org/替代 javascript 中的多或运算符/](https://www.geeksforgeeks.org/alternative-to-multiple-or-operators-in-javascript/)

在本文中，我们将学习在条件语句中使用 multiple || (OR 运算符)的替代方法。条件语句中的多个或运算符可能会导致代码可读性差，并且通常功能有限。

下面的 JavaScript 代码可以重写，以其他方式执行相同的任务:

## java 描述语言

```
let user = "motivated";
let recommended_org = "";

/* If user is a geek or motivated or
    curious then the recommended organisation
    for him/her is GeeksforGeeks */
if (user == "geek" ||
    user == "motivated" ||
    user == "curious") {
  recommended_org = "GeeksforGeeks";
  console.log(recommended_org);
}
```

**输出:**

```
GeeksforGeeks
```

**方法 1:** 这种方法使用一个 if-else 阶梯来处理所有不同的可能性。

在这种方法中，语法大量增加。由于每个 if 语句的结果都是相同的，因此最好使用使用多个 OR 运算的原始方法。

然而，随着程序在选项上变得越来越复杂，if-else 梯形更受欢迎，因为它增加了代码的可读性。它也非常灵活，因为可以添加任意数量的条件，甚至嵌套条件，由于这些原因，它可以用于复杂的条件。

下面的示例演示了这种方法:

## java 描述语言

```
/* If user is a geek or motivated or
    curious then the recommended organisation
    for him/her is GeeksforGeeks */
if (user == "geek") {
  recommended_org = "GeeksforGeeks";
}
else if (user == "motivated") {
  recommended_org = "GeeksforGeeks";
}
else if (user == "curious") {
  recommended_org = "GeeksforGeeks";
}
else {
  recommended_org = "No recommendation"
}
console.log(recommended_org);
```

**输出:**

```
GeeksforGeeks 
```

**方法 2:** 这种方法使用开关情况语句来处理所有不同的可能性。

Switch-case 语句功能强大，它们增加了代码的可读性，而且使用 default 和 break 语句使代码编写更高效。

在这种情况下，通过使用 switch-case 语句增加了语法，但是与以前的方法相比，代码的重复更少。在 if-else 阶梯中，我们使用赋值语句三次，但在这种方法中，我们只使用一次。但是嵌套开关情况会使代码变得非常复杂，并且对于有很多嵌套条件的问题，它通常不是首选，所以它没有 if-else 那么灵活。

下面的示例演示了这种方法:

## java 描述语言

```
let user = "curious";
let recommended_org = "No recommendation";

/* If user is a geek or motivated or
  curious then the recommended organisation
  for him/her is GeeksforGeeks */
switch (user) {
  case "geek":
  case "motivated":
  case "curious":
    recommended_org = "GeeksforGeeks"
    break;
  default:
    recommended_org = "No Recommendation"
}

console.log(recommended_org);
```

**输出:**

```
GeeksforGeeks
```

**方法 3:** 这种方法使用一个地图对象来处理所有不同的可能性。

这种方法非常灵活，就像 if-else 阶梯一样，并且很容易扩展，因为需要添加更多的键值对，但是在非常复杂的例子中，它仍然不能取代上述方法。

下面的示例演示了这种方法:

## java 描述语言

```
let user = "geek";

/* A recommended_org map object which consists
   the behaviour of the user as the key and the
   recommended organisation as the values */
var recommended_org = {
    "geek": "GeeksforGeeks",
    "motivated": "GeeksforGeeks",
    "curious": "GeeksforGeeks",
    "other": "No Recommendation"
}

/* if user is a geek or motivated or
   curious then the recommended organisation
   for him/her is GeeksforGeeks */
console.log(recommended_org[user] ||
  recommended_org["other"]);
```

**输出:**

```
GeeksforGeeks 
```

任何一种选择都不能称之为优越，因为所有的选择都有利弊。这取决于程序员的个人观点和使用它的环境。然而，了解可用的替代方案仍然是一种很好的做法。