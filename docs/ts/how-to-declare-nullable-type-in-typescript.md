# 如何在 TypeScript 中声明可空类型？

> 原文:[https://www . geesforgeks . org/如何声明-可空类型-键入脚本/](https://www.geeksforgeeks.org/how-to-declare-nullable-type-in-typescript/)

在普通的 JavaScript 中，有两种主要的数据类型， **null** 和 **undefined** 。以前在 TypeScript 中，不可能将这些类型显式命名为“null”和“undefined”。但是，无论类型检查模式如何，现在都可以使用它。

要将“未定义”分配给任何属性，必须关闭**–严格空值检查**标志。保持此标志为开不允许将“未定义”分配给没有可空运算符的成员。

下面的例子代表了如果启用**–严格空值检查**标志并执行以下代码会发生什么。

```
interface Student {
 name:string;
 age:number;
}

let s: Student = {
 name:'Ajay',
 age:null
}
```

它会抛出以下错误:

```
Type 'null' is not assignable to type 'number'

```

如果我们关闭了**–stringnullchecks**标志，则不会出现此错误。**严格空值检查**标志防止在代码中引用空值或未定义的值。可以通过在命令行编译器中添加**-–stringnullchecks**标志作为选项，或者将其添加到 *tsconfig.json* 文件中来启用。

可空类型和“可选”之间是有区别的。在“可选”中，我们为成员提供一些默认值，或者让它不被视为成员。但是，如果任何成员被赋予了可选值，然后仍然被赋予了“null”或“undefined”的值，那么它将抛出一个错误。

```
interface Student {
 name:string;
 age?:number;
}

let s: Student = {
 name:'Ajay',
 age:null
}
```