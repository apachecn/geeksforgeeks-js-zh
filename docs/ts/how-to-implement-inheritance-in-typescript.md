# 如何在 Typescript 中实现继承？

> 原文:[https://www . geesforgeks . org/如何实现类型脚本中的继承/](https://www.geeksforgeeks.org/how-to-implement-inheritance-in-typescript/)

继承是面向对象编程语言的主要支柱，继承用于从现有的类创建一个新的类。新创建的类称为派生类，派生类继承的类称为基类。继承的派生类获取基类的属性和行为。TypeScript 支持单继承和多继承。我们不能使用 TypeScript 实现混合和多重继承。继承使用基于类的继承，可以使用 typescript 中的**扩展**关键字来实现。在本文中，我们将看到继承是如何在 TypeScript 中实现的。

**语法:**

```
class baseClassName {
}
class derivedClassName extends baseClassName {
}
```

**TypeScript 中的单一继承:**在单一继承中，基类的属性和行为最多可以继承到一个派生类中。它用于向已经实现的类添加新功能。

**示例:**在本例中，我们创建了一个 Person 作为基类，并使用单一继承实现了 Teacher 作为派生类。

## java 描述语言

```
// Base class
class Person {
  Name: string;
  constructor(name: string) {
    this.Name = name;
  }
}
// Deriving Teacher class
class Teacher extends Person {
  Payment: number;
  constructor(name: string, payment: number) {
    super(name);
    this.Payment = payment;
  }
  display(): void {
    console.log("Teacher's Name: " + this.Name);
    console.log("Teacher's Payment " + this.Payment);
  }
}
// Create Object
let obj = new Teacher("GeeksforGeeks", 8500000);
obj.display();
```

**输出:**

```
Teacher's Name: GeeksforGeeks 
Teacher's Payment 8500000
```

**2。多级继承:**

在多级继承中，派生类充当另一个派生类的基类。新创建的派生类获取其他基类的属性和行为。

**示例:**在本例中，我们创建了一个作为基类的 Vehicle 和一个作为子类的 Car，该子类派生了名为 carModel 的新类，carModel 类获取了 Vehicle 和 Car 类的所有特性。

## java 描述语言

```
// Base class
class Vehicle {
  Type(): void {
    console.log("Car");
  }
}

// Inherites from Vehicle
class Car extends Vehicle {
  Brand(): void {
    console.log("ABC");
  }
}

// Inherites all properties of 
// Vehicle and Car class
class carModel extends Car {
  Model(): void {
    console.log("ABC2021");
  }
}

// Object creation
let obj = new carModel();
obj.Type();
obj.Brand();
obj.Model();
```

**输出:**

```
Car  
ABC
ABC2021
```