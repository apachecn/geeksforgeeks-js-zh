# 在 JavaScript 中闭包有什么实际用途？

> 原文:[https://www . geeksforgeeks . org/什么是 javascript 中的闭包实用工具/](https://www.geeksforgeeks.org/what-is-the-practical-use-for-a-closure-in-javascript/)

在 JavaScript 中，**闭包**被定义为内部函数，即使在外部函数已经返回之后，也可以访问外部函数的变量和参数。下面的例子展示了闭包的实际应用:

**示例:**在本例中，定义了一个变量 **mult** ，该变量位于函数 **multFn** 中，并且只能在该函数中访问。声明内部函数时，JavaScript 会创建一个闭包，内部函数可以访问变量及其参数。

## JavaScript

```
// Define the closure
function multFn() {
  var mult = 9;
  return function(val) {
    mult = mult * val;
    return mult;
  }
}

// Use the closure
var mult = multFn();
console.log(mult(18));
```

**输出:**

```
162
```

**1。使用私有变量和方法:**在 JavaScript 中，我们可以使用闭包来使用私有变量和方法。下面的例子展示了私有变量在闭包中的使用。

**示例:**在本例中， **rentPrice()** 函数使用三种方法返回一个对象: **getRent()、incRent()、**和**derent()**。这三种方法都有访问私有变量**租金**的权限。但是，其范围之外的代码不能直接访问该变量。因此，我们可以在 JavaScript 中模仿面向对象编程。

## java 描述语言

```
// Define the closure
var rentPrice = function(initialRent) {
   var rent = initialRent;

    // Define private variables for
    // the closure
    return {
      getRent: function() {
        return console.log(rent);
      },
      incRent: function(amount) {
        rent += amount;
        console.log(rent);
      },
      decRent: function(amount) {
         rent -= amount;
         console.log(rent);
      }
    }
}

var Rent = rentPrice(8000);

// Access the private methods
Rent.incRent(2000);
Rent.decRent(1500);
Rent.decRent(1000);
Rent.incRent(2000);
Rent.getRent();
```

**输出:**

```
10000
8500
7500
9500
9500
```

**2。维护每个函数调用之间的状态:**假设有一个函数，人们希望它将多个值相乘。这可以在全局变量的帮助下完成，因为它们在整个程序中都是可访问的。然而，一个缺点是它们容易在代码的任何地方发生变化。这可以使用闭包来完成。闭包有助于在不使用全局变量的情况下维护函数调用之间的状态。

**示例:**

## 【JavaScript】

```
(function() {

  var multFn = function multiply() {
    // This variable is local to
    // the closure and holds
    // its value inbetween
    // multiple calls
   var mult = 9;
   return function(val) {
     mult = mult * val;
     return mult;
   }
  };

  var mult = multFn();

  // Call the method
  // multiple times
  console.log(mult(2));
  console.log(mult(3));
  console.log(mult(5));
}());
```

**输出:**

```
18
54
270
```