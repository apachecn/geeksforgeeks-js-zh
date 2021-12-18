# 如何在 TypeScript 中检查接口类型？

> 原文:[https://www . geesforgeks . org/how-check-interface-in-type script/](https://www.geeksforgeeks.org/how-to-check-interface-type-in-typescript/)

Typescript 是一种纯面向对象的编程语言，由类、接口、继承等组成。它很严格，像 Java 一样静态类型化。接口用于在 typescript 中定义联系人。一般来说，它定义了实体的规范。下面是一个汽车接口或合同的例子。

```
interface Audi {
    length: number;
    width: number;
    wheelbase: number;
    price:number;
    numberOfAirBags:number;
    seatingCapacity: number;
    getTyrePressure: () => number;
}
```

**方法:**

*   Declare an interface as a string by name and type.
*   Now create a custom function to check the interface type.
*   The function returns a Boolean value if the name attribute exists in the passed parameter.
*   Now use the if statement to check the value returned by the function, and you can perform further operations on the requirements.

**例 1:**

## Javascript

```
interface Student{
    name:string;
}

var geek:any = { 
    name: "Jairam" 
    };

function instanceOfStudent(data: any): data is Student {
    return 'name' in data;
}

if (instanceOfStudent(geek)) {
    document.write("Student Name is "+ geek.name);
}
```