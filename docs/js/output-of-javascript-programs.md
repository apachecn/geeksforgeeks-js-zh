# JavaScript 程序的输出

> 原文:[https://www . geesforgeks . org/输出 javascript 程序/](https://www.geeksforgeeks.org/output-of-javascript-programs/)

**1。预测并解释下面 JavaScript 程序的输出。**

## Javascript

```
function f(a, b, c) {
    m = ["1", "2", "3"];
    a = 3;
    b[0] = "X";
    c.first = false;
}

var x = 4;
var y = ["A", "B", "C"];
var z = { first: true };

f(x, y, z);
console.log(x, y, z);

function g(a) {
    a = { first: true };
    console.log(a);
}

g(z);
console.log(z);
```

**输出:**

```
4 ["X", "B", "C"] {first:false} {first:true} {first:false}

```

**解释:**当记录(x，y，z)时，x 给出值 4(因为图元是按值传递的，因此即使在函数 f()之后，其值也不会改变)。y 是一个数组，因此是一个对象，所以它是通过引用传递的，它的索引 0 被更改为 X。所以 y 记录 X，B，c。在函数 f()中，c.first 被更改为 false，因为它是通过引用传递的，所以它首先记录:false。在函数 g()中，创建了一个值为 true 的新对象，因此它首先记录:true。最后，在最后一行，z.first 仍然等于 false，因此它记录为 first:false。

**2。预测并解释以下 JavaScript 程序的输出:**

## JavaScript

```
function foo1() {
   return {
      bar: "hello";
   };
}

function foo2() {
   return
   {
      bar: "hello";
   };
}

console.log(foo1());
console.log(foo2());
```

**输出:**{栏:“你好”}未定义

**解释:**在 foo1()中，bar 对象按其应有的方式返回，因此它给出输出{ bar:“hello”}。但是在 foo2()中，return 后的换行符有不同的解释。它在 return 后面隐式地放了一个分号，相应的一组行被视为一个语句块。所以 foo2()有下面的 return 语句——return；这给出了未定义的输出。

**3。预测并解释以下 JavaScript 程序的输出:**

## JavaScript

```
(function() {
   console.log(1);
   setTimeout(function(){console.log(2)}, 1000);
   setTimeout(function(){console.log(3)}, 0);
   console.log(4);
})();
```

**输出:** 1432

**说明:**setTimeout()函数只有在父函数完全执行并返回后才会被调用。因此，即使 console.log(3)有 0 毫秒的超时，它也只是在记录 1 和 4 之后父函数返回之后才执行。然后记录 3。最后，在 1000 毫秒的超时后，记录了 2。

**4。预测并解释以下 JavaScript 代码片段的输出:**

## JavaScript

```
for (var i = 0; i < 5; i++) {
   (function(x) {
      setTimeout(function() {
         console.log(x);
      },  1000 );
   })(i);
}
```

**输出:** 0 1 2 3 4

**解释:**借助一个立即调用的函数表达式(IIFE)，会创建它自己的作用域，我们可以把 I 传递给函数。变量 I 将是一个局部变量，每个循环中的 I 值将被保留，并在超时 1 秒后最终打印出来。

**5。预测并解释以下 JavaScript 程序的输出:**

## JavaScript

```
var x= 5;
function check(){
   y = 10;
   console.log(x);
   var x =10;
}

function check2(){
   console.log(y);
}

check();
check2();
```

**输出:**未定义 10

**说明:** var x 在记录后已在 check()内部定义并初始化。提升仅用于变量声明，而不用于初始化，因此它返回 undefined。在 check()中，y 已初始化为 10。因为没有使用 var，所以变量有它的作用域，直到它遇到一个给定名称或全局对象的变量。因此，当调用 check2()时，它会记录 10 作为输出。