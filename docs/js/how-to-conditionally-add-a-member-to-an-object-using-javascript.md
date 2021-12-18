# 如何使用 JavaScript 有条件地给对象添加成员？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 有条件地将成员添加到对象中/](https://www.geeksforgeeks.org/how-to-conditionally-add-a-member-to-an-object-using-javascript/)

对象是最重要的数据类型，也是现代 JavaScript 的构建块。它们不同于原始数据类型，如字符串、数字、布尔值、空值等。但是我们可以通过使用**新的**关键字将这些数据类型作为对象。有两种方法可以有条件地向对象添加成员。

**方法 1:** 该方法包括检查所需条件是否为真，并基于该条件向对象添加属性。

**示例:**在本例中，如果条件为真，则‘b’将作为成员添加到‘a’中，否则不添加。

## Javascript

```
// Define the object
var a = {};

// Check if the condition
// is satisfied
if (someCondition) {

    // Add the required 
    // property to the object 
    a.b = 7;
}
```