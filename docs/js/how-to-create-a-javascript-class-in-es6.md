# 如何在 ES6 中创建一个 JavaScript 类？

> 原文:[https://www . geesforgeks . org/how-create-a-JavaScript-class-in-es6/](https://www.geeksforgeeks.org/how-to-create-a-javascript-class-in-es6/)

类描述了属于它的对象的内容:它描述了一组数据字段(称为实例变量)，并定义了对这些字段的操作(称为方法)。您可以通过在类名前使用名为 class 的预定义关键字来创建一个 Javascript 类。我们将在下面展示一些例子来说明它是如何工作的。

**语法:**

```
class name {
    // body of the class
}

```

创建类的对象可以通过使用 new 关键字并调用该类的构造函数来完成。构造函数通过使用预定义的关键字构造函数来声明。构造函数可以是任何类型，例如默认构造函数和参数化构造函数。正如我们在这里看到的，我们使用构造函数来初始化和声明一个变量。但是，每个类只能有一个构造函数，并且可以参数化或默认。

**语法:**

```
class name {
   constructor(a, b, c) {
     // Initialize the class variable
   }
}

```

**例 1:**

## 超文本标记语言

```
<script>
    class Geeks {

        // Constructor
        constructor(num1, num2) {
            console.log("Inside Constructor");

            // Initialize class variable
            this.num2 = num2;
            this.num1 = num1;
        }
    }

    // Initialize the class object
    let obj = new Geeks(1, 2);
    console.log(obj.num1);
    console.log(obj.num2);
</script>
```

**输出:**

```
Inside Constructor
1
2
```

**例 2:**

## 超文本标记语言

```
<script>
    class Geeks {
        constructor(num1, num2) {
            this.num2 = num2;
            this.num1 = num1;
        }
        add() {
            console.log(
            this.num1 + "+" + this.num2 + 
            "=" + (this.num1 + this.num2));
        }
    }
    let obj = new Geeks(1, 2);
    obj.add();
</script>
```

**输出:**

```
1+2=3
```