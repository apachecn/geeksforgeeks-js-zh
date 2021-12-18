# JavaScript |将参数传递给回调函数

> 原文:[https://www . geesforgeks . org/JavaScript-将参数传递给回调函数/](https://www.geeksforgeeks.org/javascript-passing-parameters-to-a-callback-function/)

**回调函数:**
将一个函数传递给另一个函数或者将一个函数传递给另一个函数内部的函数称为**回调函数**。
换句话说，回调是一个已经定义的函数，作为参数传递给其他代码

**语法:**

```
function geekOne(z) { alert(z); }
function geekTwo(a, callback) {
    callback(a);        
}
prevfn(2, newfn);
```

以上是 JavaScript 函数中回调变量的一个例子。
*【极客一号】*接受一个参数，并生成一个以 *z* 为参数的警报。
*【极客二】*接受一个参数和一个函数。
*“geek two”*将它接受的参数移动到要传递给它的函数。
*“geek one”*就是这种情况下的回调函数。

**示例:**

```
<script>
function GFGexample(fact, callback){ 
  var myFact = "GeeksforGeeks Is Awesome, " + fact;
  callback(myFact); // 2
}

function logFact(fact){
  document.write(fact);
}
GFGexample("Learning is easy since", logFact);
</script>
```

**输出:**

```
GeeksforGeeks Is Awesome, Learning is easy since
```

**进场:**
这里*【gfgeexample】*是主要功能，接受 2 个参数，*【回调】*是第二个。 *logFact 函数*用作回调函数。当我们执行*“gfgeexample”*函数时，请注意我们没有在*日志*中使用括号，因为它是作为参数传递的。这是因为我们不想自发地运行回调，我们只需要将函数传递给我们的主函数供以后执行。
确保如果*回调*函数需要参数。然后我们在执行时提供这些参数。
而且，你不需要用*“回调”*这个词作为参数名，JavaScript 只需要知道它是正确的参数名。

JavaScript 回调函数使用起来简单高效，对于 Web 应用程序和代码非常重要。