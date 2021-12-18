# JavaScript 中有哪些类和代理？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的类和代理/](https://www.geeksforgeeks.org/what-are-the-classes-and-proxies-in-javascript/)

[**类**](https://www.geeksforgeeks.org/javascript-classes/) **:** 这些几乎和函数类似，只是用了一个 class 关键字而不是 function 关键字。函数和类的另一个重要区别是，函数可以在定义之前在代码中调用，而类必须在 JavaScript 中构造类对象之前定义，否则运行代码会抛出[引用错误。](https://www.geeksforgeeks.org/javascript-referenceerror-variable-is-not-defined/)

**定义类:**可以通过使用 class 关键字和构造函数来初始化类来定义类。

**语法:**

```
class Classname {
    constructor(property1, property2) {
        this.property1 = property1;
        this.property2 = property2;
    }
}
```

**示例:**以下示例描述了一个简单的类。

## Java Script 语言

```
<script>
    class Employee {
        constructor(name, id) {
            this.name = name;
            this.id = id;
        }
    }
    let Employee1 = new Employee("Suraj", 533);
    console.log(Employee1);
</script>
```

**输出:**

```
Employee {name: 'Suraj', id: 533}
id: 533
name: "Suraj"
[[Prototype]]: Object
```

**类表达式:**我们也可以使用[类表达式](https://www.geeksforgeeks.org/javascript-class-expression/)定义一个类。它们可以有两种类型，即“已命名”或“未命名”。一个类的名称可以通过***名称*** 属性来访问。

**语法:**

```
let Employee = class {
      constructor(name, id) {
          this.name = name;
          this.id = id;
      }
}
```

**示例:**

## Java Script 语言

```
<script>

   // Unnamed class
    let Employee1 = class {
        constructor(name, id) {
            this.name = name;
            this.id = id;
        }
    }
    console.log(Employee1.name);   

   // Named class
    let Employee2 = class Intern {
        constructor(name, id) {
            this.name = name;
            this.id = id;
        }
    }
    console.log(Employee2.name);        
</script>
```

**输出:**

```
Employee1
Intern
```

**类方法:**我们也可以在类内部定义方法。它可以有也可以没有参数。

**语法:**

```
class Classname {
 constructor(property1, property2) {
   this.property1 = property1;
   this.property2 = property2;
 }
 method1() { ... }
}
```

**示例:**

## Java Script 语言

```
<script>
    class Employee {
        constructor(name, id) {
            this.name = name;
            this.id = id;
        }

        // Without parameter
        getname(){
            return "Name of Employee: "+this.name; 
        }

        // With parameter
        getdept(department){
            return "Works in " + department;
        }
    }

    let Employee1 = new Employee("Suraj", 533);
    console.log(Employee1.getname());
    console.log(Employee1.getdept("Finance department"));
</script>
```

**输出:**

```
Name of Employee: Suraj
Works in Finance department
```

**Proxis:** [代理](https://www.geeksforgeeks.org/javascript-proxy-object/)是用于重新定义对象基本操作的对象。它允许我们创建另一个对象的代理。

**参数:**

代理对象接受下面描述的两个参数:

*   **目标:**是我们要用代理包装的原始对象。
*   **处理程序:**如果在代理上执行操作，其属性定义代理行为的对象。

**语法:**

```
const target = {
   property1: "first property",
   property2: "second property"
};
const handler = { ... };
const proxy1 = new Proxy(target, handler);
```

**示例:**

## Java Script 语言

```
<script>
    const target = {
        property1: "GeeksforGeeks",
        property2: "Computer science portal"
    };

    const handler = {};
    const proxy = new Proxy(target, handler);

    console.log(proxy.property1); 
    console.log(proxy.property2); 
</script>
```

**输出:**

```
GeeksforGeeks
Computer science portal
```

因为处理程序是空的，所以它不影响目标。因此，代理表现为其原始目标。

我们还可以在处理程序中定义操作，将代理的属性从其原始目标更改。为此，我们需要使用 [**get()**](https://www.geeksforgeeks.org/javascript-handler-get-method/) 处理程序，该处理程序可以访问目标的属性并操纵代理内部的属性。 [**反映**](https://www.geeksforgeeks.org/javascript-reflect-get-method/) 类有助于将目标的原始属性应用于代理。

**示例:**我们在处理程序中应用了 [if](https://www.geeksforgeeks.org/if-else-statement-in-javascript/) 条件，以检查目标的“property2”，输出应该从目标的原始属性更改。

## Java Script 语言

```
<script>
    const target = {
        property1: "GeeksforGeeks",
        property2: "Computer science portal"
    };

    const handler = {
        get: function (target, prop, receiver) {
            if (prop === "property2") {
                return "For computer science geeks";
            }
            else{
                return Reflect.get(target,prop);
            }
        }
     }
        const proxy = new Proxy(target, handler);

        console.log(proxy.property1); 
        console.log(proxy.property2); 
</script>
```

**输出:**

```
GeeksforGeeks
For computer science geeks
```