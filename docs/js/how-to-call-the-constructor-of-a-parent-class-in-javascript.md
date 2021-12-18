# 如何在 JavaScript 中调用父类的构造函数？

> 原文:[https://www . geesforgeks . org/如何调用 javascript 中父类的构造函数/](https://www.geeksforgeeks.org/how-to-call-the-constructor-of-a-parent-class-in-javascript/)

在本文中，我们学习如何调用父类的构造函数。在本文开始之前，我们应该对 javascript 有一个基本的了解，以及 javascript 中继承的一些基本概念。

**构造函数:**构造函数创建类的实例，这些实例通常被称为对象。JavaScript 中的 new 关键字导致在声明对象时调用构造函数。构造函数创建一个对象，并设置任何存在的对象属性。

**JavaScript 中的继承:**一个对象访问另一个对象的属性和方法的能力称为继承。对象可以从其他对象继承属性和方法。JavaScript 通过原型继承属性，这种形式的继承通常被称为原型继承。

**JavaScript 中的 super 关键字:**通过在构造函数方法中执行 Super()方法，我们调用父级的构造函数方法，获得对父级的属性和方法的访问。我们只能在父类的子类中使用 super 关键字。

现在让我们通过例子来理解如何调用父类的构造函数。

**示例:**在本例中，我们将使用两个类一个用于父类，另一个用于子类，用于继承父类的属性和方法，因此我们必须使用 extends 关键字从父类继承子类。然后在子类构造函数中，我们必须调用父类构造函数，否则编译器会通过一个错误，告诉您在访问它之前，在子类构造函数方法中提及或调用构造函数。

## Java Script 语言

```
<script>
    class Geeks {
        constructor(num1) {
            this.num1 = num1;
        }
        fun() {
            console.log("Parent class method call");
        }
    }
    class Myclass extends Geeks {
        constructor(num1, num2) {

            // Calling parent class constructor
            super(num1);
            this.num2 = num2;
        }
        fun() {
            super.fun();
            console.log("child class method call");
        }
    }
    let obj = new Myclass(1, 2);
    obj.fun();
</script>
```

**输出:**

```
Parent class method call
child class method call
```

**示例 2:** 在调用 super 之前，这不能在子类构造函数中使用。在 ES6 中，子类的构造函数需要调用 super，或者它们必须返回一些对象来代替从未初始化的对象。在这个例子中，极客类是我的类的父类，当一个对象被创建为我的类类型时，它首先调用我的类构造函数中的我的类构造函数，在访问“this”(自己的对象)之前，我们必须调用父类构造函数。所以它首先调用父类(极客类)构造函数，然后再访问自己的对象。

## Java Script 语言

```
<script>
    class Geeks {
        constructor(num) {
            this.num = num;
            console.log("inside Parent Class constructor");
        }
    }
    class MyClass extends Geeks {
        constructor(num1, num2) {
            super(num1);
            this.num2 = num2;
            console.log("inside Child class Constructor");
        }
    }
    let obj = new MyClass(1, 2);
</script>
```

**输出:**

```
inside Parent Class constructor
inside Child class Constructor
```