# 打字稿中有哪些环境？

> 原文:[https://www . geesforgeks . org/什么是环境类型脚本/](https://www.geeksforgeeks.org/what-are-ambients-in-typescript/)

Typescript 提供了一种使用第三方库的方法，如 Node.js、jQuery、AngularJS 等。以更容易和更安全的方式。这些是在环境声明的帮助下完成的。

环境声明是一种通知 TypeScript 编译器真实源代码(如函数或变量)存在于另一个地方的方法。如果我们试图利用这些在运行时不存在的源代码，那么如果不给出提示，它就会被破坏。如果我们的 TypeScript 代码需要使用第三方 JavaScript 库，如 jQuery、AngularJS、Node.js 等，我们必须始终编写环境声明。

当使用这些 JavaScript 库(如 jQuery、AngularJS、Node.js 等)时，验证代码的完成和类型安全性对于 TypeScript 程序员来说变得很困难。因此，环境声明有助于将其他 JavaScript 库直接集成到 TypeScript 中。

**定义环境声明:**环境声明文件必须以扩展名**保存。在扩展名为 **d.ts** 的环境声明文件中，每个根级别定义前面必须有 **declare** 关键字。作者将被清除，不会有任何由 TypeScript 发布的代码。作者需要确认在运行时声明的项目将存在。**

环境声明文件类似于文档文件(如果源发生变化，文档文件需要保持更新)。因此，如果环境声明文件没有更新，那么它们将返回编译错误。按照惯例，环境声明文件保存在扩展名为的类型声明文件中，如下所示:

```
Trial.d.ts
```

以上文件不能**转编译**成 JavaScript 文件。可用于代码完成和类型安全。

现在要声明环境方法和变量，我们必须使用**声明**关键字。声明环境变量或环境声明的语法如下所示:

**语法:**

```
declare module module_name {
}
```

下面给出了在客户机类型脚本文件中提到环境文件的语法:

```
/// <reference path = "Trial.d.ts" />
```

**特征:**以下是 TypeScript 中环境的特征:

*   环境声明允许安全地使用现有的非常好的 JavaScript 库。
*   环境声明有助于将其他 JavaScript 库直接集成到 TypeScript 中..
*   环境声明是告诉编译器现有变量/函数/等等的一种方式。
*   在环境声明中有一个 declare 关键字，这意味着我们声明了一个变量的类型而没有它们的实现，TypeScript 只是假设我们会以某种方式组成那个实现(通过添加一个脚本标签或者我们拥有的任何自定义编译器)。

**应用程序:**TypeScript 中的 Ambients 用于描述没有用 TypeScript 编写的库的形状，为此我们必须声明库揭示的 API。这是因为几乎没有任何顶级对象被 JavaScript 库揭示，一种更好的表示它们的方法是名称空间。

我们在环境声明中调用了一个 declare 关键字，这意味着我们声明了一个变量的类型而没有它们的实现，TypeScript 只是假设我们会以某种方式组成那个实现(通过添加一个脚本标签或者我们拥有的任何自定义编译器)。通常，它们在. d.ts 文件中描述。因此，我们必须编写一个环境模块来为已经用 JavaScript 编写的代码编写类型声明。如上所述，这些是在以. d.ts 文件扩展名结尾的文件中定义的。

所以从根本上说，环境声明是由编译器做出的保证。如果第三方库在运行时不存在，如果我们试图使用它们，那么事情就会毫无征兆地中断。

**示例 1:** 要理解环境声明，请查看下面给出的示例。这里，第三方 JavaScript 库与下面给出的代码一起使用:

## java 描述语言

```
var TestSum;    
(function (TestSum) {    
   var Calc = (function () {   
      function Calc() {   
      }   
      Calc.prototype.doSum = function (x, z) {  
         return x + z;  
      }  
   })  
})
```

作为一个 JS 文件，我们没有时间将这个库重写为 typescript。但是，您确实需要添加带有类型安全的 **doAdd()** 功能，那么通过使用**环境声明**我们可以做到这一点。所以，现在我们将创建一个环境声明文件。

## java 描述语言

```
declare module TestAdd{   
   export class Calc {   
      doAdd(x:number, z:number) : number;   
   }  
}
```

现在，我们将在 typescript 文件中包含这个环境声明文件(CalAdd.d.ts)。如下所示–

## 主. ts

```
var obj = new TestAdd.Calc();   
console.log("Add: " +obj.doAdd(60, 15));
```

现在，通过在控制台上使用以下命令，编译并执行 Main.ts 文件:

```
$ tsc main.ts
$ node Main.js

```

**输出:**我们将得到如下输出:

```
75
```

**示例 2:** 要理解环境声明，请查看下面给出的示例。这里，第三方 JavaScript 库与下面给出的代码一起使用:

## java 描述语言

```
var TestDif;
(function (TestDif) {    
   var Calc = (function () {   
      function Calc() {   
      }   
      Calc.prototype.doDif = function (x, z) {  
         return x - z;  
      }  
   })  
})
```

作为一个 JS 文件，我们没有时间将这个库重写为 typescript。但是，您确实需要添加带有类型安全的 **doSubtract()** 函数，那么通过使用环境声明，我们可以做到这一点。所以，现在我们将创建一个环境声明文件。

## java 描述语言

```
declare module TestDif{   
   export class Calc {   
      doSubtract(x:number, z:number) : number;   
   }  
}
```

现在，我们将在 typescript 文件中包含这个环境声明文件。如下所示:

## 主. ts

```
var obj = new TestDif.Calc();   
console.log("Subtract: " + obj.doSubtract(50, 10));
```

现在，通过在控制台上使用以下命令，编译并执行 Main.ts 文件:

```
$ tsc main.ts 
$ node Main.js

```

**输出:**我们将得到如下输出:

```
40
```