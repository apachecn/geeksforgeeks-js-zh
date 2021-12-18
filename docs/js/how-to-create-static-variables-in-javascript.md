# 如何在 JavaScript 中创建静态变量？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中创建静态变量/](https://www.geeksforgeeks.org/how-to-create-static-variables-in-javascript/)

在本文中，我们将学习在 JavaScript 中创建静态变量。

**静态关键字在 JavaScript 中:***静态*关键字用于定义一个 [**静态方法**](https://www.geeksforgeeks.org/static-methods-in-javascript/) 或者一个类的属性。要调用静态方法，我们不需要创建类的实例或对象。

**JavaScript 中的静态变量:**我们使用了 *static* 关键字来使变量静态，就像使用[T5【const】T6](https://www.geeksforgeeks.org/javascript-const/)T8 关键字来定义常量变量一样。它是在运行时设置的，这种类型的变量作为*全局*变量工作。我们可以在任何地方使用静态变量。与常量变量不同，静态变量的值可以重新分配。

**我们为什么在 JavaScript 中创建静态变量:**我们在 JavaScript 中创建静态变量是为了防止复制，固定配置，它对缓存也很有用。

**示例 1:** 在下面的示例中，我们将创建一个静态变量，并将其显示在 JavaScript 控制台上。

## java 描述语言

```
<script>
 class Example {
   static staticVariable = 'GeeksforGeeks';

  //static variable defined
   static staticMethod() {
     return 'static method has been called.';
      }
  }
  // static variable called
  console.log(Example.staticVariable);
  // static method called
  console.log(Example.staticMethod());

</static>
```

**输出:**

![](img/dc3c11f576e0a4aaef6b90c1c60648d7.png)

静态法

**例 2:** 静态变量叫做使用 [*这个*](https://www.geeksforgeeks.org/this-in-javascript/) 关键字。

## java 描述语言

```
<script>
  class Example {
    static staticVariable = 'GeeksforGeeks';
   //static variable defined
   static staticMethod() {
     return 'staticVariable : '+this.staticVariable;
      }
  }
  // static method called
  console.log(Example.staticMethod());
</script>
```

**输出:**

![](img/d1d519d09ee05bb12c1ba784d55874e9.png)