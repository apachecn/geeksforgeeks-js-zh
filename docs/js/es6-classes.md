# 是 6 |班

> 原文:[https://www.geeksforgeeks.org/es6-classes/](https://www.geeksforgeeks.org/es6-classes/)

面向对象编程**对象**、**类**和**方法**中有三个概念。ES6 JavaScript 支持面向对象编程组件。

*   **对象:**实时对象实体是指任何实体的实时呈现。
*   **类:**是创建任何对象的计划之前，这些对象被称为您要创建的任何对象的蓝图。
*   **方法:**在物体之间进行交流。

该类包含**构造函数**和**函数**。构造函数负责为类的对象分配内存。该函数负责对象的动作。将这两个**建造师**和**功能**组合在一起，组成**类**。
在 ES6 中创建任何类，都需要使用 **class** 关键字。
**语法:**
声明类:

```
class Class_name {  
}
```

类表达式:

```
var var_name = new Class_name {  
}
```

以下示例将说明 ES6 类:
**示例:**

## java 描述语言

```
<script>
class gfg {

    // Constructor
    constructor(name, estd, rank){
        this.n = name;
        this.e = estd;
        this.r = rank;
    }

    // Function
    decreaserank(){
        this.r -= 1;
    }
}
const geeks = new gfg("geeks", 2009, 43)

geeks.decreaserank();

document.write(geeks.r); //Output 42
</script>
```

**输出:**

```
42
```

上面给出的例子声明了一个类“gfg”。该类的构造函数接受三个参数——名称、estd 和等级。“this”关键字引用了类的当前实例。geeks()函数在类中，打印排名的值。
**类继承:**ES6 类支持继承。继承有勇气从现有的实体创建实体。ES6 中有两种类型的类:

*   **父类/超类:**扩展创建新类的类称为父类或超类。
*   **子/子类:**新创建的类称为子类或子类。子类继承父类的所有属性，除了构造函数

**语法:**

```
class child_name extends parent_name
```

**例:**

## java 描述语言

```
<script>
class geeks {
   constructor(g) {
      this.Character = g
   }
}
class GeeksforGeeks extends geeks {
   disp() {
      console.log("No of Character:  "+this.Character)
   }
}
var obj = new GeeksforGeeks(13);
obj.disp()
</script>
```

**输出:**

```
No of Character: 13
```

继承分为三种类型:

*   **单一继承:**每个类都可以从一个父类扩展而来。
*   **多重继承:**一个类可以从多个类继承。ES6 不支持多重继承。
*   **多级继承:**一个类可以从从父类继承的另一个类(via)继承。

```
class Child extends Root
class Leaf extends Child 
// So the leaf extends root indirectly
```

**Super 关键字:**该关键字帮助子类调用父类数据。

```
supper.object
```

**例:**

## Java Script 语言

```
<script>
class GeeksforGeeks {
   doPrint() {
      console.log("This doPrint() from Parent called.")
   }
} 
class gfg extends GeeksforGeeks {
   doPrint() {
      super.doPrint()
      console.log("This doPrint() is printing a string.")
   }
}
var obj = new gfg()
obj.doPrint()
</script>
```

**输出:**

```
This doPrint() from Parent called.
This doPrint() is printing a string.
```