# JavaScript |嵌套类

> 原文:[https://www.geeksforgeeks.org/javascript-nested-classes/](https://www.geeksforgeeks.org/javascript-nested-classes/)

让我们试着去理解，什么是阶级。JavaScript 中的类是一种函数，可以通过 function 关键字和 class 关键字进行初始化。在本文中，我们将通过函数关键字的使用来介绍 javascript 中的内部类。这里有一个使用 function 关键字的类的例子。

**示例:**

```
<!DOCTYPE html>
<html>
    <head>
        <title>Class as a function</title>
        <meta charset="utf-8" />
        <script>

            // Write Javascript code here
            function Employee() {

                // Here we have created a property
                // name of class Employee;
                this.name = ""; 
                this.employeeId = 0;
            }

            // An (global) object of type Employee
            // is created.
            var emp = new Employee(); 

            emp.name = "miss anonymous";
            emp.employeeId = 101;
            function showName() {
                alert(emp.name);
            }
        </script>
    </head>
    <body>
        <button type="button" onclick="showName()">
          Click Me
        </button>
    </body>
</html>
```

**输出:**

```
miss anonymous
```

类作为函数和函数的区别在于，我们在函数定义中使用了这个关键字，使其作为类工作。现在，内部类以类似的方式定义。

正如您在这段代码中看到的，我们已经在其中创建了一个外部类和内部类，就像我们之前做的一样。但是，要访问外部类的属性，我们需要对象的地址。这是唯一正确的方法。正如你在上面的例子中看到的，为了访问外部类的属性 x，我们使用了变量 objOuterClass(它存储了类的当前实例的地址)，并且使用对象的地址，我们可以很容易地访问内部类中外部类的任何属性或方法。

现在，在尝试访问内部类的成员或属性时，可以应用同样的技巧。如您所见，我们已经在内部类之外创建了一个内部类对象。所以每次创建外部类的对象时，我们都在创建内部类的对象，并将其地址存储在变量 innerObj 中。

**示例:**

```
<!DOCTYPE html>
<html>
    <head>
        <title>Inner class in JS</title>
        <meta charset="utf-8" />
        <script>
            function OuterClass() {

            // Property x of OuterClass
            this.x = 0; 
            this.y = 30;

            // Assign the variable objOuterClass the address 
           // of the particular instance of OuterClass
            var objOuterClass = this; 

            // Inner class
            function InnerClass() {
              this.z = 10;
              this.someFuncton = function () {
                  alert("inner class function");
                    }; 

             // Assign the address of the anonymous function.
             // to access the value of property of outer class 
             // in inner class.
               this.accessOuter = function () {
                  alert("value of x property:" + objOuterClass.x);
                    };
             } 

                // InnerClass ends to access the inner class 
                // properties or methods.
                this.innerObj = new InnerClass();
            }

          function show() {
             var outerClassObj = new OuterClass();
            alert("Inner class Property z:" + outerClassObj.innerObj.z);
            }
        </script>
    </head>

    <body>
        <button type="button" onclick="show()">
         Click Me
        </button>
    </body>
</html>
```

**输出:**

```
Inner class Property z:10
```