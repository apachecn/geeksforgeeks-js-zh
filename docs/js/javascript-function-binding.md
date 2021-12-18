# JavaScript |函数绑定

> 原文:[https://www.geeksforgeeks.org/javascript-function-binding/](https://www.geeksforgeeks.org/javascript-function-binding/)

在 JavaScript 中，函数绑定是使用 **Bind()** 方法进行的。通过这种方法，我们可以将一个对象绑定到一个公共函数上，这样函数在需要的时候就会给出不同的结果。否则，它会在代码执行时给出相同的结果或错误。
我们使用 **Bind()** 方法调用一个带有**这个**值的函数，*这个*关键字指的是当前选中的同一个对象。换句话说， **bind()** 方法允许我们在调用函数或方法时，轻松设置哪个对象将被*这个*关键字绑定。
绑定的需求通常会出现，当我们在一个方法中使用 *this* 关键字，并且我们从一个接收者对象调用该方法时，那么有时候 *this* 并没有绑定到我们期望绑定的对象。这导致了我们程序中的错误。

现在，调用函数 *printFunc()* 时，一个简单的程序打印这个关键字调用的名称。

```
<script>
var geeks = {
name : "ABC",
printFunc: function(){
   document.write(this.name);}
   }

  geeks.printFunc();
</script>
```

**输出:**

```
ABC
```

这里访问名称**“ABC”**、*这个*关键字将*名称*变量绑定到函数是没有问题的。它被称为默认绑定。*这个*关键词指的是**极客**对象。

现在看下面的代码，

```
<script>
var geeks = {
name : "ABC",
printFunc: function(){
   document.write(this.name);}
   }

  var printFunc2= geeks.printFunc;
  printFunc2();
</script>
```

**输出:**

```
//no output is produced by this code//
```

这里我们做了一个新的变量函数 *printFunc2* ，指的是对象*极客*的函数 *printFunc()* 。这里*这个*的绑定丢失，所以不产生输出。
为了确保*这个*的任何绑定都不会丢失，我们使用 **Bind()** 方法。
通过使用 *bind()* 方法，我们可以将*这个*的上下文设置为特定的对象。因此，我们也可以使用其他变量来调用绑定函数。

使用上例中的 **bind()** 方法:

```
<script>
var geeks = {
name : "ABC",
printFunc: function(){
   document.write(this.name);}
   }

  var printFunc2= geeks.printFunc.bind(geeks);
   //using bind() 
   // bind() takes the object "geeks" as parameter//
  printFunc2();
</script>
```

**输出:**

```
ABC
```

**bind()** 方法创建了一个新函数，其中**这个**关键字引用了上例**极客**括号中的参数。通过这种方式， **bind()** 方法能够调用具有指定的**这个**值的函数。

**示例 4:**
在这个示例中有 3 个对象，每次我们使用 **bind()** 方法调用每个对象。

```
<script>
//object geeks1
var geeks1 = {
name : "ABC",
article: "C++"
}
//object geeks2
  var geeks2 = {
name : "CDE",
article: "JAVA"
}

  //object geeks3
  var geeks3 = {
name : "IJK",
article: "C#"
}

function printVal(){
   document.write(this.name+" contributes about "+this.article+"<br>");
   }

  var printFunc2= printVal.bind(geeks1);
   //using bind() 
   // bind() takes the object "geeks1" as parameter//
  printFunc2();

  var printFunc3= printVal.bind(geeks2);
  printFunc3();

  var printFunc4= printVal.bind(geeks3);
  printFunc4();
  //uniquely defines each objects
</script>
```

**输出:**

```
ABC contributes about C++
CDE contributes about JAVA
IJK contributes about C#
```