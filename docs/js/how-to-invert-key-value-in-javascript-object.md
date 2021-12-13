# 如何在 JavaScript 对象中反转键值？

> 原文:[https://www . geesforgeks . org/如何在 javascript 对象中反转键值/](https://www.geeksforgeeks.org/how-to-invert-key-value-in-javascript-object/)

JavaScript 是一种高级的、解释的和动态类型的客户端脚本语言。JavaScript 用于向静态 HTML 添加动态特性。在 JavaScript 中，一切都是一个对象。JavaScript 中的对象可以用方括号{..}并且对象可以包括某些属性。这些属性基本上是键值对。密钥是用于存储和检索值的标识符。使用传统方法反转键-值对是乏味的。但是随着“下划线. js”的出现，键值的反转可以使用内置的方法 **_。invert()** 。在本文中，我们将讨论两种反转 JavaScript 对象键值对的方法。

**第一种方法:**在本例中，我们将演示反转键值对的传统方法。首先，创建一个具有属性“姓名”、“年龄”、“标准”和“费用”的学生对象。定义了一个**逆()**函数，该函数以学生对象为参数，循环遍历对象的每个键。定义了一个新的对象 *retobj* ，它存储反转的键值对。

**代码实现:**

## Javascript

```html
function inverse(obj){
  var retobj = {};
  for(var key in obj){
    retobj[obj[key]] = key;
  }
  return retobj;
}

var student = 
{
    name : "Jack",
    age: 18,
    std : 12,
    fees : 5000
}
console.log("Object before inversion");
console.log(student);
student = inverse(student);
console.log("Object after inversion");
console.log(student);
```