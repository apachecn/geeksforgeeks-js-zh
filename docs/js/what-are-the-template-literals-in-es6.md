# ES6 中有哪些模板文字？

> 原文:[https://www . geesforgeks . org/什么是模板文字-in-es6/](https://www.geeksforgeeks.org/what-are-the-template-literals-in-es6/)

**模板文字**是编程中用来表示某种固定值的文字，模板是指可以生成某种实体的蓝图，因此，模板文字用于生成固定值的字符串。我们可以在其中插入 JavaScript 表达式和字符串。

**语法:**

```
`Any string ${jsExpression} can appear here`
```

**示例:**在本例中，我们演示了模板文字的简单演示。

## Javascript

```
<script>
const str1 = `Hi, GeeksforGeeks Learner`;
console.log(str1);

const str = "GeeksforGeeks";
const str2 = `Hi, ${str} Learner`;
console.log(str2);
</script>
```