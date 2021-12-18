# JavaScript ES6 中的箭头操作符

> 原文:[https://www . geesforgeks . org/arrow-operator-in-es6-of-JavaScript/](https://www.geeksforgeeks.org/arrow-operator-in-es6-of-javascript/)

ES6 有各种各样的优点，其中之一就是箭头操作符。它减少了定义代码大小的函数，因此它是访谈中提出的趋势问题之一。让我们更深入地了解箭头操作器的功能。
**语法:**
在 ES5 中，函数由以下语法定义:

```
function functionName(arg1, arg2….)
{
    // body of function
}

```

但是在 ES6 中，使用箭头运算符定义了一个函数，其语法如下:

```
const functionName = (arg1, arg2 ….) => {
    // body of function
}

```

**箭头操作符的优点:**
**1)减少代码大小:**
由于我们已经用相应的箭头操作符替换了函数，因此代码的大小减少了，我们必须为相同的工作编写更少的代码。这就是为什么我喜欢定义函数的箭头运算符方法。
**2)删除一行函数的函数括号:**
我们可以删除箭头运算符声明中函数的括号，例如:
**代码#1:**

```
<script>

   //ES5 VERSION
   var setSize = (sz)=>
   size=sz;

   //sets size value to the passed value
   setSize(10);
   document.write(size);

</script>
```

**输出:**

```
10
```

这也可以写成:
**代码#2:**

```
<script>

    //ES6 Version 
    //Do not need to put curly braces for one line functions
    setDoubleSize = (sz)=>size=2*sz;

    //Sets value of size equivalent to double of
    //passed argument in setDoubleSize function
    setDoubleSize(35);
    document.write(size);    

</script>
```

**输出:**

```
70
```

**3)无需在一行中定义 return 语句函数:**
在 ES5 中，您必须在函数中定义 return 语句，如果在 ES6 中我们没有定义 return 语句，那么每当调用给定函数时，ES6 都会自动返回值。
这将通过下面的例子来说明:
ES5 版本的一位左移功能如下:

```
function leftShift(value)
{
    return value / 2;
}
```

而在 ES6 中，以下函数可以写成如下形式:

```
var leftShift = (value) => value / 2;
```

**代码#3:**

```
<script>

    //ES5 VERSION
    function leftShiftES5(value){
    return value/2;
    }

    //ES6 VERSION
    var leftShiftES6 = (value)=>value/2;
    var a=10,b=10;
    document.write('values before left shift'+"<br>");
    document.write('a : '+a+' b : '+b + "<br>");

    //Both of the function should give same output 
    a=leftShiftES5(a);
    b=leftShiftES6(b);
    document.write('values after left shift' +"<br>");
    document.write('a : '+a+' b : '+b + "<br>");

</script>
```

**输出:**

```
values before left shift
a : 10 b : 10
values after left shift
a : 5 b : 5

```

**4)词汇绑定上下文:**
Arrow 运算符词汇绑定上下文，因此这是指起始上下文。这意味着它使用箭头函数。我们考虑一个有年龄数组的类，如果年龄< 18，我们将把它们推入子队列。在 ES5 中，您必须按如下方式进行:

```
this.age.forEach(function(age) {
    if (age < 18)
        this.child.push(age);
}.bind(this));
```

在 ES6 中，这可以通过以下方式完成:

```
this.age.forEach((age) => {
    if (age < 18)
        this.child.push(age);
});
```

因此，我们不必隐式绑定它，这是通过箭头函数自动完成的。
所以我们已经看到箭头函数使函数编写变得不那么复杂，并且减少了行数，所以它被开发人员的问题所使用，并且它也是面试中最热门的问题之一。