# TypeScript 中接口和类型有什么区别？

> 原文:[https://www . geesforgeks . org/type script 中接口和类型的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-interface-and-type-in-typescript/)

方法**类型**和**界面**都用于描述类型脚本中对象的结构。但是拥有一些特定的特性，这些特性会根据情况有所帮助，在它们之间进行选择完全取决于开发者。

**类型脚本中的类型:**类型脚本中的类型系统描述了语言支持的不同数据类型。分为**任意类型**、**内置类型**和**自定义类型**三大部分。TypeScript 中的类型系统负责检查任何取值的数据类型，然后才能将其作为程序的输入。

**示例:**

```
// Creating a type
type Geeks {
  name: string;
  age: number
}

type Geeks {
  email: string;
}

// Using the merged type
const gfg: Geeks = {
  name: " kgowda",
  age: 20,
  email: " kgowda@gmail.com"
};

console.log(gfg);
```

**输出:**

```
"Duplicate identifier 'Geeks'" error.
```

**类型脚本中的接口:**类型脚本中的接口是所有实体都必须遵守的语法义务。它只能包含成员的声明，负责定义**属性**、**方法**和**事件**。在某种程度上，它负责定义派生类必须遵循的标准结构。

**示例:**

```
// Creating a interface
interface Geeks {
  name: string;
  age: number
}

interface Geeks {
  email: string;
}

// Using the merged interface
const gfg: Geeks = {
  name: " kgowda",
  age: 20,
  email: " kgowda@gmail.com"
};

console.log(gfg);
```

**输出**

```
name: " kgowda", age: 20, email: " kgowda@gmail.com"
```

**类型脚本中类型和接口的区别:**

| 类型 | 连接 |
| --- | --- |
| 它是数据类型的集合。 | 这是一种语法形式。 |
| 它支持为类型创建新名称。 | 它提供了一种定义实体的方法。 |
| 相对而言，它的能力更弱。 | 它有相对更多的能力。 |
| 它不支持使用对象。 | 它支持对象的使用。 |
| 不能使用多个合并声明。 | 可以使用多个合并声明。 |
| 两个同名的类型会引发异常。 | 两个同名的接口被合并。 |
| 它没有实现目的。 | 它有一个实现目的。 |