# 类型脚本环境声明

> 原文:[https://www . geesforgeks . org/typescript-ambients-declaration/](https://www.geeksforgeeks.org/typescript-ambients-declaration/)

typescript 中的环境声明用于告诉 Typescript 编译器实际代码存在于其他地方。第三方库是用普通的 JavaScript 或者像 jquery/anglarjs/nodejs 这样的 CoffeeScript 编写的，虽然这是我们使用 TypeScript 所需要的，但是我们总是可以编写环境声明并使用它们。

**环境声明:**
环境声明的文件扩展名为(d.ts)。对于每个根级别定义，文件扩展名(d.ts)必须有 declare 关键字才能在 Typescript 中使用。

如果我们试图使用运行时不存在的源代码，那么程序将在没有警告的情况下中断。

环境声明文件类似于文档文件。当来源改变时，文档需要保持更新。否则，如果环境声明文件没有更新，我们将得到编译器错误。

> . d.ts 文件

我们无法将上述文件转换成 JavaScript。上述文件将用于类型安全和智能感知。
使用 declare 关键字，可以声明环境变量和方法。
环境声明的语法是:
**语法:**

```
declare module module_name{  
}  

```

**访问环境文件的语法:**

环境声明可以通过以下示例来理解。下面，我们使用第三方 JavaScript 库，包含以下代码。
**例:**

```
var TestSum;    
(function (TestSum) {    
   var Cal = (function () {   
      function Cal() {   
      }   
      Cal.prototype.doSum = function (a, b) {  
         return a + b;  
      }  
   })  
})  
```

由于这是一个 JS 文件，我们没有时间将这个库重写为 typescript。但是仍然需要使用带有类型安全的 doAdd()函数，那么我们可以通过使用环境声明来做到这一点。让我们创建一个环境声明文件。

```
declare module TestAdd{   
   export class Cal {   
      doAdd(a:number, b:number) : number;   
   }  
}  
```

现在，将这个环境声明文件(CalAdd.d.ts)包含到我们的 TypeScript 文件中。

```
Main.ts

```

```

var obj = new TestAdd.Cal();   
console.log("Add: " +obj.doAdd(40, 25)); 
```

在控制台上使用以下命令编译并执行 Main.ts 文件:

```
 $ tsc main.ts  
 $ node Main.js 

```

**输出:**
我们将得到如下输出。

```
65

```