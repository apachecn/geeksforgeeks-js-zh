# 如何在 ES6 中创建类？

> 原文:[https://www.geeksforgeeks.org/how-to-create-a-class-in-es6/](https://www.geeksforgeeks.org/how-to-create-a-class-in-es6/)

编程中的一个**类**是创建一个对象的蓝图或模板，每个对象代表可区分的现实世界实体。在 ES6 中，只需编写 *class* 关键字就可以创建类。在本文中，我们将讨论类的一般概念及其语法以及相关示例。

在 ES6 中有两种创建类的方法，要么在类定义之前编写类关键字，要么将类表达式赋给变量。

**方法 1:类声明**在这个方法中，我们只需编写代码，并添加关键字 Class 作为类名的前缀。

**语法:**

```
class ClassName {
    // Definition and code
}
```

**示例:**在这个示例中，我们已经声明了一个类，在这个类中，有两个 getter 和 setter 方法以及一个构造函数。稍后在类声明之外，我们通过向构造函数提供半径来创建该类的对象，在下一行中，我们只是提取圆的面积属性。

**注意:** *ES6* 有不同种类的特殊语法来创建 getter 和 setter。就像我们首先写*获取*或*设置*关键字，然后写属性的名称。在 get 的情况下，我们从这个方法返回的任何东西都被认为是对象的属性的值，而在 set 的情况下，我们作为参数提供的任何东西都可以被设置为构造函数内部编写的任何属性。在属性之前写下划线是为了避免命名冲突，否则它将一次又一次地调用同一个函数。避免在 getter 方法后面放括号，因为它会抛出一个错误，即函数没有被定义，因为它被认为是对象的属性。

## 超文本标记语言

```
<script>
    class Circle {
        constructor(radius) {
            this.radius = radius;
        }

        get radius() {
            return this._radius;
        }

        set radius(r) {
            this._radius = r;
        }

        get area() {
            return ((22/7)*this.radius*this.radius);
        }
    }

    let myCircle = new Circle(5);
    console.log(myCircle.area);
</script>
```

**输出:**

```
78.57142857142857
```

**方法 2:** **类表达式**在这个方法中，我们编写类定义，并将其分配给某个变量，它可以是两种类型:命名类或未命名类。

**语法:**

```
const VariableName = class ClassName {
   // Definition and code
}

const VariableName = class {
   // Definition and code
}
```

**示例:**在这个示例中，我们已经将我们的类分配给了一个变量，现在这个变量将用于访问类，这是一个未命名的类，在这里我们也可以创建一个命名的类，但是没有这么大的区别。在类表达式中，我们已经声明了构造函数以及 getter 和 setter。稍后在类外部，有一个没有初始化的对象创建，之后，我们通过 setter 设置半径，在最后一行，我们通过 getter 访问 area 属性，该属性又返回计算的面积。

## 超文本标记语言

```
<script>
    const Circle = class {
        constructor(radius){
            this.radius = radius;
        }

        get radius() {
            return this._radius;
        }

        set radius(radius) {
            this._radius = radius;
        }

        get area() {
            return ((22/7)*this.radius*this.radius);
        }
    }

    let myCircle = new Circle();
    myCircle.radius = 3;
    console.log(myCircle.area);
</script>
```

**输出:**

```
28.285714285714285
```