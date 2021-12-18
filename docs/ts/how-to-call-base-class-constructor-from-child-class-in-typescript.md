# 如何在 TypeScript 中从子类调用基类构造函数？

> 原文:[https://www . geeksforgeeks . org/如何从 typescript 中的子类调用基类构造函数/](https://www.geeksforgeeks.org/how-to-call-base-class-constructor-from-child-class-in-typescript/)

在本文中，我们将学习如何从子类调用基类构造函数。当一个类继承另一个类的属性时，称为**子**类，其属性被继承的类称为**父**类，整个过程称为**继承**。在继承中，子类获取基类或父类的属性。

您可以使用[**【super()**](https://www.geeksforgeeks.org/javascript-super-keyword/)从子类调用基类构造函数，该函数将执行基类的构造函数。

**例:**

## Javascript

```
class Person {

  // Properties of the Person class
  Name: string;
  Profession: string;

  // Constructor of Person class
  constructor(name: string, profession: string) {
    this.Name = name;
    this.Profession = profession;
  }
}

class Details extends Person {

  // Properties of the class
  Name: string;
  Profession: string;

  // Constructor of the Details class
  constructor(name: string, profession: string) {

    // Calling the base class constructor
    super(name, profession);

    // Setting the properties
    this.Name = name;
    this.Profession = profession;
  }

  details(): string {
    return this.Name + " is " +
      this.Profession;
  }
}

// Creating an object
var data =
  new Details("A", "Android Developer");
var data2 =
  new Details("B", "Web Developer");

// Accessing the function details() 
// and printing
console.log(data.details());
console.log(data2.details());
```