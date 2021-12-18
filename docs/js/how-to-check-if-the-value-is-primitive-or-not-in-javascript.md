# 如何在 JavaScript 中检查值是否为原语？

> 原文:[https://www . geesforgeks . org/如何检查值是否是 javascript 中的原始值/](https://www.geeksforgeeks.org/how-to-check-if-the-value-is-primitive-or-not-in-javascript/)

在本文中，我们将了解如何检查一个值是否为基元。

JavaScript 提供了六种类型的原始值，包括*数字、字符串、布尔、未定义、符号*和*大整数*。基元值的大小是固定的，因此 JavaScript 将基元值存储在调用堆栈(执行上下文)中。

当我们访问一个基元值时，我们操纵存储在该变量中的实际值。因此，原始变量是由值访问的**。当我们将一个存储原始值的变量赋给另一个变量时，存储在该变量中的值被创建并复制到新变量中。**

为了检查一个值是否是原始的，我们使用以下方法:

**方法 1:** 在这种方法中，我们使用运算符的*类型来检查值的类型。如果值的类型是“对象”或“函数”，则该值不是基元，否则该值是基元。但是*运算符的*类型显示空值是一个“对象”，但实际上，空值是一个原语。*

**示例:**

## java 描述语言

```
let isPrimitive = (val) => {

  if(val === null){
      console.log(true);
      return;
  }

  if(typeof val == "object" || typeof val == "function"){
    console.log(false)
  }else{
    console.log(true)
  }
}

isPrimitive(null)
isPrimitive(12)
isPrimitive(Number(12))
isPrimitive("Hello world")
isPrimitive(new String("Hello world"))
isPrimitive(true)
isPrimitive([])
isPrimitive({})
```

**输出:**

```
true
true
true
true
false
true
false
false
```

**方法 2:** 在该方法中，我们传递**对象()**内部的值，并检查该值是否等于**对象(值)。**如果该值相等，则该值是原始值，否则不是原始值。

**示例:**

## java 描述语言

```
let isPrimitive = (val) => {

  if(val === Object(val)){
    console.log(false)
  }else{
    console.log(true)
  }
}

isPrimitive(null)
isPrimitive(12)
isPrimitive(Number(12))
isPrimitive("Hello world")
isPrimitive(new String("Hello world"))
isPrimitive(true)
isPrimitive([])
isPrimitive({})
```

**输出:**

```
true
true
true
true
false
true
false
false
```