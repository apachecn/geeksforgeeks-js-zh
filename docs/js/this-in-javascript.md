# 这在 JavaScript 中

> 原文:[https://www.geeksforgeeks.org/this-in-javascript/](https://www.geeksforgeeks.org/this-in-javascript/)

JavaScript 中的**这个**关键字经常给语言初学者带来很多困惑。这种混乱源于这样一个事实，即在 JavaScript 中的**这个**与在 Java 或 Python 中的 self 等其他语言相比被区别对待。
理解**为了理解 JavaScript 中更高级的概念或读写 JavaScript 代码，这个**是绝对必要的，这就是为什么我们将在本文中试图阐明这在 JavaScript 中的真正含义。
我们将在本文的大部分时间里学习**这个**是关于 JavaScript 中的函数的，这就是为什么我们将首先看一个关于 JavaScript 函数的事实，它将帮助我们做得更好。

这和功能

在 JavaScript 中，函数本质上是对象。像对象一样，它们可以分配给变量，传递给其他函数，并从函数中返回。就像物体一样，它们有自己的属性。其中一个属性就是**这个**。
这个存储的**值是 JavaScript 程序的当前执行上下文。因此，当在函数**中使用时，该**的值将根据该函数的定义、调用方式和默认执行上下文而变化。
**注意:** **这个**总是保存对一个**单个**对象的引用，该对象定义了当前代码行的执行上下文。
在我们进一步深入研究它在函数中的行为之前，让我们看看它在函数外的行为:
**全局上下文:**
在函数外编写的一行代码被称为属于**全局上下文**，这个在这个全局上下文中的值与全局对象相同。
例如，如果您打开浏览器控制台，并在其中键入以下几行，然后按下 return/enter:
console . log(this)
您将看到窗口对象被登录到控制台。这是因为全局对象，在浏览器运行时，如 Chrome 的运行时，是窗口对象。
但是，在函数内部，全局上下文可能不再存在，函数可能有自己定义的上下文，因此有不同的值。为了理解这一点，让我们把注意力转向函数:
函数，在 JavaScript 中可以通过多种方式调用:
1。函数调用
2。方法调用
3。构造函数调用** 

### 这与函数调用有关:

函数调用指的是使用函数的名称或表达式调用函数的过程，该表达式的计算结果为函数对象，后跟一组开括号和闭括号(包含括号表示我们要求 JavaScript 引擎立即执行该函数)。
例如:

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    function doSomething() {
        // do something here
    }

// function invocation
doSomething();
</script>                   
</body>
</html>
```

**doSomething 函数内部的这个**，如果通过上述函数调用来调用，则具有全局对象的值，即浏览器环境中的**窗口**对象:

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    function doSomething(a, b) {

       // adds a propone property to the Window object
        this.propone = "test value";
    }

// function invocation
doSomething();
document.write(window.propone);
</script>                   
</body>
</html>                       
```

**输出:**

```
test value 
```

然而，情况并非总是如此。如果 doSomething()函数在**严格**模式下运行，它将记录**未定义**而不是全局窗口对象。这是因为，在严格模式下(用线表示:**‘使用严格’；**)，这个默认值，对于任何函数对象都设置为 undefined 而不是全局对象。
例如:

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    function doSomething() {
        // enable the strict mode
        'use strict';

       // logs undefined
        document.write(this + '<br>')
            function innerFunction() {
              // Also logs undefined, indicating that
              // strict mode permeates to inner function scopes
                document.write(this)
            }
        innerFunction();
    }

// function invocation
doSomething();
</script>                   
</body>
</html>                                          
```

**输出:**

```
undefined
undefined 
```

### 这与方法调用有关:

当函数被定义为对象的字段或属性时，被称为方法。

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let person = {
        name : "John",
        age : 31,
        logInfo : function() {
            document.write(this.name + " is " + this.age + " years old ");
        }
    }
       // logs John is 31 years old
       person.logInfo()
                 </script>                   
</body>
</html>                                       
```

**输出:**

```
John is 31 years old 
```

在上面的代码示例中， **logInfo()** 是 **person 对象**的一个方法，我们使用对象调用模式来调用它。
也就是说，我们使用[属性访问器](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors)来访问作为对象一部分的方法。
这样的调用需要使用一个表达式，该表达式计算出我们的方法所属的对象，以及一个属性访问器(如: **person.logInfo()** )后跟一组左右括号。
理解函数调用和方法调用的区别是很重要的。
这反过来将帮助我们理解在任何给定的函数中**这个**上下文可能是什么，因为在这些调用的每一个中，**这个**的值是不同的。
在这样一个已经使用属性访问器调用的方法里面，**这个**会有调用对象的值，也就是**这个**会指向和属性访问器一起使用的对象来进行调用。
例如:

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let add = {
        num : 0,
        calc : function() {

            // logs the add object
            document.write(this + ' ')
                this.num
                += 1;
            return this.num;
        }
    };

// logs 1
document.write(add.calc() + '<br>');
// logs 2
document.write(add.calc());
</script>                   
</body>
</html>
```

**输出:**

```
[object Object] 1
[object Object] 2 
```

在上面的示例中，calc()是 add 对象的一个方法，因此使用第 9 行和第 10 行中的方法调用规则进行调用。
我们知道，当使用方法调用模式时，这个的值被设置为调用对象。
在这个 calc()方法中，它的值被设置为调用对象，在我们的例子中是 add。因此我们可以成功地访问 add 的 num 属性。
但是，让我们知道看看一个主要的混淆点:
嵌套在对象方法中的函数中的**这个**会发生什么？

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let add = {
        num : 0,
        calc : function() {

        // logs the add object
        document.write(this + ' ')

        function innerfunc() {
            this.num += 1;

        // logs the window object
        document.write(this + ' ');

        return this.num

    } return innerfunc();
     }
};

// logs NaN
document.write(add.calc() + '<br>');

// logs NaN
document.write(add.calc());
</script>                
</body>
</html>                              
```

**输出:**

```
[object Object] [object Window] NaN
[object Object] [object Window] NaN 
```

让我们试着理解刚刚发生了什么。
当我们在第 14 行和第 15 行调用 calc()时，我们使用的是方法调用，它设置**这个**来添加 calc()。这可以使用第 4 行的 log 语句来验证。
但是，innerfunc()是使用简单的函数调用从 calc()方法中调用的(第 11 行)。这意味着，在 innerfunc()内部，它被设置为没有 num 属性的全局对象，因此获得了 NaN 输出。
我们如何解决这个问题？我们如何从嵌套函数内部的外部方法中保留这个值？
一种解决方案是将外部函数中的**这个**值分配给嵌套函数中使用的变量，如下所示:

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let add = {
        num : 0,
        calc : function() {

            // logs the add object
            document.write(this + ' ')

           // using thisreference variable to
           // store the value of this
           thisreference = this;

            function innerfunc()
            {

             // using the variable to access the
             // context of the outer function
                thisreference.num += 1;

               // logs the add object
                document.write(thisreference + ' ');
                return thisreference.num;
            }
            return innerfunc();
        }
    };

// logs 1
document.write(add.calc() + '<br>');

// logs 2
document.write(add.calc());
</script>                   
</body>
</html>                                               
```

**输出:**

```
[object Object] [object Object] 1
[object Object] [object Object] 2 
```

这个问题的其他解决方案包括使用 bind()，call()或 apply()，我们将很快对此进行研究。

### 这与构造函数调用有关:

当 new 关键字后跟一个函数名以及一组左括号和右括号(带或不带参数)时，将执行构造函数调用。
例如:让 person1= new People('John '，21)；
这里，person1 是新创建的对象，People 是用于创建该对象的构造函数。
构造函数调用是 JavaScript 中创建对象的几种方式之一。
当我们使用新的关键字与函数名结合时，到底会发生什么？
通过这种方法创建一个对象基本上有五个步骤。让我们用下面的例子来研究它们:

## Java Script 语言

```
<!DOCTYPE html>
<html>
<body>
<script>
let people = function(name, age) {
         this.name = name;
         this.age = age;

    this.displayInfo = function() {
       document.write(this.name + " is " + this.age + " years old");
      }
    }

let person1
    = new people('John', 21);

// logs John is 21 years old
person1.displayInfo();
</script>        
</body>
</html>                                                                                  
```

**输出:**

```
John is 21 years old 
```

*   首先，创建一个空对象，它是与 new 一起使用的函数名的实例(即:people(姓名，年龄))。换句话说，它将对象的构造函数属性设置为调用中使用的函数(人员(姓名、年龄))。

*   然后，它将构造函数的原型(人)链接到新创建的对象，从而确保该对象可以继承构造函数的所有属性和方法

*   然后，在这个新创建的对象上调用构造函数。如果我们回忆一下方法调用，我们会发现是相似的。因此，在构造函数中，**这个**获取调用中使用的新创建的对象的值。

*   最后，创建的对象及其设置的所有属性和方法被返回给人员 1

**支持的浏览器:**

*   谷歌 Chrome
*   微软边缘
*   火狐浏览器
*   歌剧
*   旅行队