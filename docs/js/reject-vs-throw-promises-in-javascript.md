# 拒绝 Vs 在 JavaScript 中抛出承诺

> 原文:[https://www . geesforgeks . org/reject-vs-throw-promises-in-JavaScript/](https://www.geeksforgeeks.org/reject-vs-throw-promises-in-javascript/)

本文介绍了 Javascript 中**拒绝**和**抛出**前提的用法，并解释了它们的区别。
**reject():** 这是 Javascript 中的一个内置函数，它返回一个 Promise 对象，该对象由于特定的原因而被拒绝。

**语法:**

```
Promise.reject(reason)
```

**示例:****原因**可以是简单的**字符串消息**或者您甚至可以传递一个**错误**对象。

*   **程序 1:** 传递**字符串消息**作为**原因**。

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

   reject( 'promise failed!' );

});
p.catch(err => {

    console.log( err );

});
</script>
```

*   **输出:**

```
promise failed!
```

*   **程序 2:** 通过的**实例**错误**作为**原因**。**

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

   reject( new Error( 'promise failed!' ) );

});
p.catch( err => {

    console.log( err );

});
</script>
```

*   **输出:**如您所见，当我们通过一个**错误**对象时，我们得到了整个**错误树**。因此，用户更喜欢哪一个取决于用户。

```
Error: promise failed!
    at :4:9
    at new Promise ()
    at :2:11
    at render (tryit.php:202)
    at tryit.php:170
    at dispatch (jquery.js:4435)
    at r.handle (jquery.js:4121)
```

**抛出:**在 JavaScript 中用于创建和抛出用户定义的异常。使用 **JavaScript 抛出**语句，可以完全控制程序流程并生成用户定义的错误消息。如果我们在上面两个例子中用**扔**代替**拒绝()**的话，结果会完全一样(你可以直接用**扔**代替**拒绝**自己试试)。
**举例:**然而**抛出**可以用在**任何一个 Javascript 试捕块**中，而且不能只带承诺。

*   **程序 1:** 使用抛出承诺。

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

   throw( 'promise failed!' );

});
p.catch(err => {

    console.log( err );

});
</script>
```

*   **输出:**

```
promise failed!
```

*   **程序 2:** 使用无承诺投掷。

## java 描述语言

```
<script>
var a = 20;
try
{
  if( a < 25 )

    throw ( 'Less than 25' );

  console.log( 'Okay!' );
}
catch(err)
{
  console.log( err );
}
</script>
```

*   **输出:**现在我们已经了解了**拒绝**和**抛出**的基本工作原理，让我们来谈谈它们之间的区别:

```
Less than 25
```

**承诺-拒绝和抛出的比较:**
**1。**如果在 Promise 中有一个**异步回调函数，那么我们**就不能在回调函数**中使用 throw，因为它将**不被 catch()** 识别，并且我们将在输出中得到一个错误。**

*   **程序 1:**

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

    // Asynchronous function called within the Promise.
    setTimeout( () => { 
      throw( 'promise failed!' );

    }, 1000);
  });

  // The catch block will not be able to recognize the
  // error thrown. It will become an uncaught exception.
  p.catch( ( err )=> {

    console.log( err );
  });
</script>
```

*   **输出:**如你所见错误信息**(“承诺失败！”)**已在输出中打印，但不是通过我们承诺的 **catch()** 功能打印的。它成为一个**未捕获的异常**。

```
/home/akarshan/Desktop/Projects/Personal/gfg/app.js:3
      throw( 'promise failed!' );
      ^
promise failed!
(Use `node --trace-uncaught ...` to show where the exception was thrown)
```

*   **程序 2:** 为了解决上述情况，我们可以使用 **reject()** 方法。

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

    // Asynchronus function called within the Promise.
    setTimeout( () => {

      reject( 'promise failed!' );

    }, 1000);
  });

  // The catch block will be able to recognize
  // the rejected statement.
  p.catch( (err) => {

    console.log( err );
  });
</script>
```

*   **输出:**这里**捕捉**块能够识别**拒绝()**并打印相应的消息。

```
promise failed!
```

**2。**这是一个非常基本的区别。如果在函数内的任何地方遇到**抛出**，则立即抛出**异常**，并且**控制流程终止**。换句话说，在抛出异常**之后，控制从抛出异常**的函数中出来。

*   **程序 1:**

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

      throw( 'promise failed!' );     

      console.log("Here");
  });

p.catch( err => {
    console.log( err )
});
</script>
```

*   **输出:**从这个例子中可以清楚地看到语句 **console.log(“此处”)**没有被执行。

```
'promise failed!'
```

*   **程序 2:** 为了解决上述情况，我们使用 **reject()** 代替**抛出**函数中 **reject** 语句之后的语句将在控件进入 catch 块之前被执行。

## java 描述语言

```
<script>
const p = new Promise( ( resolve, reject ) => {

      reject( 'promise failed!' );     

      console.log( "Here" );
  });

p.catch( err => {

    console.log( err )
});
</script>
```

*   **输出:**

```
Here
promise failed!
```

**3。**T2 拒绝只能与 Javascript 承诺一起使用，但是**抛出**与拒绝**不同，可以用于在任何 try-catch 块中创建和抛出用户定义的异常，而不仅仅是带有承诺的异常**。如果在不与承诺相关联的尝试捕获块中使用 **Promise.reject()** ，将弹出**unhandledproessereject 警告**错误。

*   **程序 1:**

## java 描述语言

```
<script>
var a=20;

try{

if( a < 25 )

   Promise.reject ( 'Less than 25' );

console.log( 'Okay!' );
}
catch(err)
{
  console.log( "inside catch" );

  console.log( err );
}
</script>
```

*   **输出:**在这里，**未处理承诺对象警告**错误出现，因为**承诺.拒绝()**找不到与承诺对象相关联的捕获块。

```
Okay!
```

*   **程序 2:** 上述代码中的 catch 块与任何 Promise 对象都没有关联，因此不执行。这一点从**的输出中可以清楚地看到，因为“内部捕获”的信息没有被打印出来**。但是如果我们使用抛出，这个错误就不会发生。

## java 描述语言

```
<script>
var a=20;

try{

if( a < 25 )

  throw ( 'Less than 25' );

console.log( 'Okay!' );

}
catch(err)
{
  console.log( "inside catch" );

  console.log( err );
}
</script>
```

*   **输出:**

```
inside catch
Less than 25
```