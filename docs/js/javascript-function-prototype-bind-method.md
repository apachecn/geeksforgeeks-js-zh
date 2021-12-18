# JavaScript 函数. prototype.bind()方法

> 原文:[https://www . geesforgeks . org/JavaScript-函数-原型-绑定-方法/](https://www.geeksforgeeks.org/javascript-function-prototype-bind-method/)

A [函数](https://www.geeksforgeeks.org/functions-in-javascript/)是一组接受输入、进行一些特定计算并产生输出的语句。在编程中有各种各样的场景，我们需要预先配置**这个**关键字或函数参数，我们可以在 **bind()** 方法的帮助下，在 JavaScript 中轻松地做到这一点。bind()方法基于调用它的函数创建一个新函数。使用 bind()方法，我们可以使用下面显示的语法为函数预配置**这个**关键字和参数。

**语法:**

```
const newFunction = oldFunction.bind(thisArg, arg1, ag2, ..., argN)
```

使用上述语法，基于旧函数创建一个新函数，该关键字设置为 *thisArg* 、*T3，函数参数预配置为 *arg1* 、 *agr2* 等等。下面提到的例子通过一个例子演示了 **bind()** 方法的使用。*

**例:**

## Javascript

```
<script>
    const car = {
        brand: 'Lamborghini',
    };

    // As of now, 'this' keyword refers
    // to 'window' object.
    const printDetail = function (model, topSpeed) {
        console.log(`${this.brand} ${model} has a
        top speed of ${topSpeed} mph`);
    };

    // Calling the function without using bind which
    // means 'this' still refers to 'window' object
    // so accessing this.brand will give undefined
    printDetail('Diablo Coatl', 239);

    // Creating a new function based on printDetail
    // with 'this' keyword referring to car object
    // so accessing this.brand will give 'Lamborgini'
    const lamboPrintDetail = printDetail.bind(car);
    lamboPrintDetail('Diablo VTTT', 222);

    // Creating another function based on printDetail
    // with it's arguments pre-configured and 'this'
    // keyword referring to car object
    const reventonPrintDetail
        = printDetail.bind(car, 'Reventon', 221);

    // Since the arguments are preconfigured so we don't
    // need to pass any argument to call this function
    reventonPrintDetail();
</script>
```

**输出:**

```
undefined Diablo Coatl has a top speed of 239 mph
Lamborghini Diablo VTTT has a top speed of 222 mph
Lamborghini Reventon has a top speed of 221 mph
```