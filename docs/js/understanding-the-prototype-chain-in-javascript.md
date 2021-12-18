# 理解 JavaScript 中的原型链

> 原文:[https://www . geesforgeks . org/了解原型-javascript 中的链/](https://www.geeksforgeeks.org/understanding-the-prototype-chain-in-javascript/)

当你开始学习编程时，你会遇到面向对象编程这个术语。在这里，我们发现了它的含义，您承认它是用于将数据分组为具有属性的“对象”。
在很多编程语言中创建这些对象的关键字是类。您可以使用构造函数和许多其他公共和个人函数来定义一个类别。如果希望一个类从另一个类继承，可以编写简单的继承语法。您已经创建了一个继承序列。直到 2015 年，该语言才实现了一个类别。相反，他们使用原型链。新的 ES6“类”隐藏了原型链的内部工作。如果你想在使用 JavaScript 的 OOP 范例的同时开发高性能的代码，理解原型链是至关重要的。对于熟悉(或不太熟悉)计算的人来说，原型链可能是一个链表。这是一个严重的过度简化。

**我们如何初始化我们的链？**
JavaScript 中的所有对象都有一个原型。物体的原型也被认为是物体。

```
function Dog(name) {
  this.name = name;
}
```

因为原型是一个对象，所以原型有自己的原型。这样的话，Dog.prototype 的原型就是 *Object.prototype*

```
// Returns true
Object.prototype.isPrototypeOf(Dog.prototype);
```

**输出:**

```
 true

```

回想一下 **hasOwnProperty()** 方法。

## java 描述语言

```
let duck = new Dog("Donald");
duck.hasOwnProperty("name"); // yields true
```

**输出:**

```
  true

```

**hasOwnProperty()** 方法在 *Object.prototype* 中定义，可由 *Dog.prototype* 访问，然后可由变量“duck”访问。它清楚地解释了原型链。在这个原型链中，“狗”是“鸭”的超类型，而“鸭”是子类型。对象是“狗”和“鸭”的超类型。我们认为对象是 JavaScript 中所有对象的超类型。任何对象都可以使用**HasownProperty()**JavaScript 方法。