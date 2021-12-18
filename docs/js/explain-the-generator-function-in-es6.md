# 解释 ES6

中的发电机功能

> 原文:[https://www . geesforgeks . org/explain-the-generator-function-in-es6/](https://www.geeksforgeeks.org/explain-the-generator-function-in-es6/)

ES6 引入了一个新的概念，称为生成器(或生成器函数)。它为您提供了一种使用迭代器和函数的新方法。ES6 生成器是一种新型的功能，可以在中间暂停，也可以在中间多次暂停，稍后再恢复。在标准函数中，控制保留在被调用函数中，直到它返回，但是 ES6 中的生成器函数允许调用函数控制被调用函数的执行。

生成器和常规函数的区别在于:

*   作为对生成器调用的响应，它的代码不会运行。取而代之的是，它返回一个名为“生成器对象”的特殊对象来管理执行。
*   生成器函数可以随时将控件返回(或让出)给调用者。
*   与常规函数不同，生成器可以根据需要返回(或产生)多个值。

**语法:**生成器函数的语法与常规函数相似。唯一的区别是，生成器函数在函数关键字后用星号(*)表示。

```
function *myfunction() { }
```

**Yield 运算符:**在 Yield 语句中，函数执行暂停，并向调用者返回一个值。在这种情况下，会保留足够的状态，以便函数从停止的地方恢复。在最后一次产量运行后，函数在恢复后立即恢复执行。您可以使用此函数生成一系列值。

**JavaScript next 方法:**next()方法将在接收到参数时恢复生成器函数的执行，用 next()方法的参数替换暂停执行的 yielded 表达式。next()方法返回的对象总是有两个属性。

*   价值——产出的价值就是价值。
*   完成-函数的完成状态可以表示为布尔值 true。否则，它会产生错误。

**示例:**在本例中，我们取一个生成器函数并生成 3 个数字，连续调用生成器函数 4 次以查看实际输出，总之，我们看到当我们第四次调用生成器函数时，它给出的值为 undefined，done 属性为 true。因为在这次调用中，生成器函数已经完成了三个连续数字的生成，所以当我们第四次调用该函数时，它没有给出任何值，并将完成状态更新为真，这意味着第四次没有要生成的值。

## Java Script 语言

```
<script>
    function* generator() {
        yield 1;
        yield 2;
        yield 3;
    }
    let obj = generator();
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
</script>
```

**输出:**

```
{
  done: false,
  value: 1
}
{
  done: false,
  value: 2
}
{
  done: false,
  value: 3
}
{
  done: true,
  value: undefined
}
```

**生成器函数中的 Return 语句:**Return 语句将指定的值发送回其调用方。它结束函数调用的执行，并将结果返回给调用方。在 return 语句之后定义的语句不会在函数中执行。因此，return 语句应该出现在函数的末尾。

**示例 2:** 这里我们使用第三行的 return 语句来看看 return 在生成器函数中是如何工作的。通常情况下，当我们在 return 语句之后写任何语句时，它会给出一个错误，但是在 return 语句之后写任何 yield 语句时，它不会给出任何错误，除了它显示生成器函数调用结束之外，它意味着没有进一步的步骤来生成数字。

## Java Script 语言

```
<script>
    function* generator() {
        yield 1;
        yield 2;
        return 3;
        yield 4;
    }
    let obj = generator();
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
</script>
```

**输出:**

```
{
  done: false,
  value: 1
}
{
  done: false,
  value: 2
}
{
  done: true,
  value: 3
}
{
  done: true,
  value: undefined
}
```

**调用另一个生成器函数内部的生成器函数来生成函数:**我们可以使用 *yield ** 运算符(或语句)来调用另一个生成器函数内部的生成器函数。

**示例 3:** 在本例中，我们使用 yield *语句在另一个生成器函数内部调用一个生成器函数。有两个生成器函数，一个名为*生成器*，另一个名为 *myfunction* ，这两个函数都是参数函数。这里我们通过调用并将参数传递给生成器函数来创建一个生成器函数的对象，在*生成器*函数内部，我们将使用 yield *运算符来调用 *myfunction* ，这是一个生成器函数。

## Java Script 语言

```
<script>
    function* myfunction(k) {
        yield k + 1;
        yield k + 2;
        yield k + 3;
    }
    function* generator(i) {
        yield i;
        yield* myfunction(i);
        yield i + 5;
    }
    let obj = generator(6);
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
    console.log(obj.next());
</script>
```

**输出:**

```
{
  done: false,
  value: 6
}
{
  done: false,
  value: 7
}
{
  done: false,
  value: 8
}
{
  done: false,
  value: 9
}
{
  done: false,
  value: 11
}
{
  done: true,
  value: undefined
}
```