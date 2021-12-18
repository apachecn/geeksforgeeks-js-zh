# JavaScript 中的箭头功能

> 原文:[https://www . geesforgeks . org/arrow-functions-in-JavaScript/](https://www.geeksforgeeks.org/arrow-functions-in-javascript/)

先决条件:[这个在 JavaScript 中](https://www.geeksforgeeks.org/this-in-javascript/)
在这篇文章中，已经讨论了一些与 JavaScript 中**这个**相关的更多功能。

### 这和箭头功能:

ES6 中引入的箭头函数提供了一种用 JavaScript 编写函数的简洁方法。
它提供的另一个显著优势是，它不绑定自己的**这个**。换句话说，箭头函数内部的上下文是由词汇或静态定义的。
这是什么意思？
与其他函数不同，这个内部箭头函数的值不依赖于如何调用或如何定义它们。它只依赖于它的封闭上下文。
我们用一个例子来试着理解一下:

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let People = function(person, age) {
        this.person = person;
        this.age = age;
        this.info = function() {

         // logs People
         document.write(this);

         setTimeout(function() {
            // here this!=People
           document.write(this.person + " is " + this.age +
                                              " years old");
          }, 3000);
        }
    }
   let person1 = new People('John', 21);

// logs : undefined is undefined years old after 3 seconds
person1.info();
</script>     
</body>
</html>
```

**输出:**

```
[object Object] 
undefined is undefined years old
```

之所以我们得到未定义的输出，而不是正确的信息作为输出，是因为定义为 setTimeout 回调的函数()有一个正常的函数调用，正如我们所知，这意味着它的上下文被设置为全局上下文，或者换句话说，它的值被设置为窗口对象。
之所以会出现这种情况，是因为每个常规的非箭头函数都根据它们的调用来定义自己的 This 或 context。封闭对象/函数的上下文不会影响自动定义它们自己的上下文的趋势。
我们如何解决这个问题？
想到的一个显而易见的解决方案是，如果函数没有定义自己的上下文会怎样？如果它从 info()继承了上下文，会怎么样，因为这意味着这个函数()得到了 info()
中定义的 this，这正是箭头函数所做的。他们从他们的封闭的
上下文中保留了这个的价值。
也就是说，在上面的例子中，如果为 setTimeout()定义为回调的函数是一个箭头函数，它将从它的封闭上下文–info()
中继承该函数的值

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let People = function(person, age) {
        this.person = person;
        this.age = age;
        this.info = function() {

            // logs People
            document.write(this);

           setTimeout(() => {
            // arrow function to make lexical "this" binding
            // here this=People."this" has been inherited
            document.write(this.person + " is " + this.age
                                           + " years old");
           }, 3000);
        }
    }
let person1 = new People('John', 21);

// logs : John is 21 years old after 3 seconds
person1.info();
</script>                   
</body>
</html> 
```

**输出:**

```
[object Object] 
John is 21 years old
```

因此，不管 arrow 函数是使用函数调用还是方法调用来调用的，它都会从其封闭上下文中保留这个的]值。换句话说，箭头函数的这个值与其外部的值相同。
如果在任何封闭函数之外使用，箭头函数会继承全局上下文，从而将其值设置为全局对象。

### 这在单独的方法中:

当来自任何对象的方法与其分离，或者存储在变量中时，例如:let separated = People.info，它会丢失对其调用对象的引用。
注意信息后缺少左右括号。这表明我们没有立即调用该方法。
例如:

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let People = function(person, age) {
        this.person = person;
        this.age = age;
        this.info = function() {

            // logs People
            document.write(this + ' ');

            // here this=People
            document.write(this.person + " is " + this.age +
                                      " years old" + '<br>');
        }
    }

let person1
    = new People('John', 21);

// logs : John is 21 years old
person1.info();

// separating the method info() from its
// object by storing it in a variable
let separated = person1.info;

// logs : undefined is undefined years old
separated();
</script>                   
</body>
</html>
```

**输出:**

```
[object Object] John is 21 years old
[object Window] undefined is undefined years old
```

一旦我们将 info()与 person1 对象分开存储，就会丢失对 person1 对象的所有引用。
我们不能再在分离方法内部使用这个来访问父对象，因为分离方法的上下文被重置为全局上下文。
因此，当我们调用 separated()时，我们看到这现在被设置为全局窗口对象。
我们如何解决这个问题？
一种方法是将方法分开存储时，**将对象的值与方法绑定。这确保了所有对此的引用都引用此绑定对象，即使在分离的方法中也是如此。
这可以使用 bind()来完成，如:** 

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let People = function(person, age) {
        this.person = person;
        this.age = age;
        this.info = function() {

            // logs People
            document.write(this + ' ');

            // here this=People
            document.write(this.person + " is " + this.age +
                                    " years old" + '<br>');

        }
    }

let person1
    = new People('John', 21);

// logs : John is 21 years old
person1.info();

let separated = person1.info.bind(person1);

/*
the bind(person1) statement ensures that "this" always
refers to person1 inside the bound method- info()
*/

// logs : undefined is undefined years old
separated();
</script>                   
</body>
</html>
```

**输出:**

```
[object Object] John is 21 years old
[object Object] John is 21 years old
```

注意:我们可以使用任何对象将()绑定到方法信息()，而不是 code.person1，并且输出会相应地改变。将方法绑定到其父对象并不是强制性的。
如果你已经走到这一步，你会注意到我们提到 bind()几次。
现在让我们研究一下 bind()，call()和 apply()到底是什么。

### 绑定、调用和应用

bind()，call()和 apply()都用于修改函数的上下文。所有这三个都有助于明确指定这个在函数中的值。
但是，它们各自的工作方式有一定的差异。让我们研究一下这些差异。

#### 绑定()

bind()允许我们通过将一个对象绑定到一个函数来显式地定义这个函数内部的值。
绑定对象用作其绑定到的函数的上下文(该值)。
要使用它，我们主要需要两样东西——一个要绑定到函数的对象和这个对象要绑定到的函数。【bind 的一般语法是:

```
boundfunction = someFunction.bind(someObject, additionalParams);
```

bind()指令中使用的第一个参数用作 this 值，其后的参数是可选的，用作绑定函数的参数。

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let fruit = function(person, color) {
        this.person = person;
        this.color = color;
        this.displayInfo = function() {
            document.write(this.person + " is " + this.color + '<br>');
        }
    }

let bindingObj
    = {
        // creating an object using object literal syntax
        person : "Banana",
        color : "Yellow",
      }

// Constructor invocation to create an object fruit1
let fruit1
    = new fruit("Orange", "orange");

// logs :Orange is orange
// Method invocation of displayInfo()
fruit1.displayInfo();

// binding the separated method to a new object
let newBound = fruit1.displayInfo.bind(bindingObj);

// logs : Banana is Yellow
newBound();
</script>                   
</body>
</html>
```

**输出:**

```
Orange is orange
Banana is Yellow
```

请注意，我们使用方法调用:水果 1.displayInfo 在水果 1 上调用 displayInfo()，因此可能期望它具有水果 1 的上下文。然而，情况似乎并非如此，因为记录的是“香蕉是黄色的”，而不是“橘子是橙色的”。
发生这种情况是因为我们使用 bindingObj 的 binding()命令在 displayInfo()中显式绑定了这个的值。
我们可以看到，将一个对象显式绑定到一个函数会覆盖它的正常上下文规则，并强制将所有这些值设置到它内部的绑定对象。
通常，当传递函数时，它会失去上下文。例如:

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let noBinding = {
        persons : "John",

        passAround() {

        // displayInfo function is passed
        // as a callback to setTimeout
        setTimeout(this.displayInfo, 3000);
        },

        displayInfo() {

        // logs the Window object
        document.write(this + ' ');

        // logs undefined
        document.write(this.persons);

        }
    }

    noBinding.passAround();
</script>                
</body>
</html>                                                        
```

**输出:**

```
[object Window] undefined
```

为了防止在作为回调传递的函数内部重置上下文，我们显式地将其值绑定为与 passAround()内部相同，即:绑定到绑定对象:

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    let binding = {
        persons : "John",

        passAround() {

            // displayInfo function is passed as a callback
            // to setTimeout binding the context of displayInfo
            // to "this" = binding in this execution context
            setTimeout(this.displayInfo.bind(this), 3000);

        },

        displayInfo() {
            // logs the binding object
            document.write(this + ' ');

            // logs John
            document.write(this.persons);

        }

    }

     binding.passAround();
</script>                   
</body>
</html>                                                       
```

**输出:**

```
[object Object] John
```

#### 调用()并应用()

调用()和 apply()执行类似于 bind 的任务，方法是显式指定它应该在函数中存储什么值。
但是，它们和 bind()的一个主要区别是，调用()和 apply()会立即调用函数，而不是简单地准备一个绑定了该值的函数副本以备将来使用。
语法:
T3】叫 :

```
function.call(thisValue, arg1, arg2, ...)
```

**敷** :

```
function.apply(thisValue, [ arg1, arg2, ...])
```

这两种情况下的第一个参数是我们希望被调用函数具有的值。
本质上，这两种方法的唯一区别是，在 apply 中，第二个参数是参数的数组对象，而在 call 中，所有参数都以逗号分隔的格式发送。
例如:

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<script>
    // Create two different objects to test call() and apply()
    let banana = { person : 'Banana' };
let orange = { person : 'Orange' };
function fruits(adj)
{
    document.write(this + ' ');
    return (this.person + " is " + adj + '<br>');
}

  // call() and apply() will immediately invoke
  // the function they are being called on

  // logs : Banana is yummy
  document.write(fruits.call(banana, 'yummy'));

 // logs: Orange is sour
  document.write(fruits.apply(orange, [ 'sour' ]));
</script>                   
</body>
</html>                                                      
```

**输出:**

```
[object Object] Banana is yummy
[object Object] Orange is sour
```

**注意**:call()和 apply()都是默认 Function 对象原型上可用的方法。

### 这与事件侦听器有关

在用作事件侦听器回调的函数中，它保存触发事件的元素的值。

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<button>Click me to see console logging < /button>
<script>
    let elem = document.querySelector('btn')
        elem.addEventListener('click', function() {
        // logs: btn
       document.write(this)
     })
</script>                  
</body>
</html>
```

如果这里使用的回调函数是一个箭头函数，并且我们的事件侦听器嵌套在另一个方法中，这将引用外部嵌套方法的上下文，并且我们不能再访问事件侦听器使用它添加到的元素，就像我们在前面的代码示例中一样。
幸运的是，这可以通过对像这样的元素使用 currentTarget 方法来轻松解决:

## java 描述语言

```
<!DOCTYPE html>
<html>
<body>
<button>Click me to see console logging < /button>
<script>
function outerfunc(elem)
{

    this.clickHandler = function() {
    elem.addEventListener('click', (e) => {

       // logs the<button />element
      document.write(e.currentTarget);

   // this has the value of outerfunc
this.displayInfo();
})
}
;
this.displayInfo = function() {
    document.write(' Correctly identified!');
}
}

let button = document.body.querySelector('button');
let test = new outerfunc(button);
test.clickHandler()
</script>                   
</body>
</html>                                                  
```

**输出:**

```
[object HTMLButtonElement] Correctly identified!
```

正如我们所看到的，使用 currentTarget 允许我们访问添加了事件侦听器的元素，同时这允许我们访问封闭函数的上下文——即:这允许我们成功调用 displayInfo()方法。

**支持的浏览器:**

*   Chrome 45 及以上
*   边缘 12 及以上
*   Firefox 22 及以上版本
*   歌剧 32 及以上
*   Safari 10 及以上