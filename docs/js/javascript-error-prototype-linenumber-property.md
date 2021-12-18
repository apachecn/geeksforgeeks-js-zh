# JavaScript 错误.原型.行号属性

> 原文:[https://www . geesforgeks . org/JavaScript-error-prototype-line number-property/](https://www.geeksforgeeks.org/javascript-error-prototype-linenumber-property/)

在 JavaScript 中，Error.prototype.lineNumber 属性帮助我们确定代码中的哪一行对应于错误。需要注意的一点是，该属性没有被广泛使用，因为它不是一个标准特性。

**语法:**

```
errorVariable.lineNumber
```

**例 1:**

## Javascript

```
var ex_variable = 2;
var er = new Error("Example Error");
if (ex_variable > 1) {
  throw er;
}
// Error is in the 5th line so log will show 5
console.log("Error is in line number " + er.lineNumber);
```