# JavaScript AggregateError 对象

> 原文:[https://www . geeksforgeeks . org/JavaScript-aggregateerror-object/](https://www.geeksforgeeks.org/javascript-aggregateerror-object/)

JavaScript**AggregateError**对象用于反映许多单个错误的整体错误。当需要以组合错误的形式表示多个错误时，可以使用此选项，例如，当传递给它的所有承诺都被拒绝时，可以由 *Promise.any()* 抛出。

**构造:**构造器 **AggregateError()** 用于创建 AggregateError 的新对象。

**实例属性:**该对象有两个属性:

*   **消息:**我们使用**聚合错误.原型.消息**来显示错误消息。显示的默认错误信息是 **" "** 。
*   **名称:**我们使用**aggregateerror . prototype . name**来显示错误的名称。显示的默认错误名称是 AggregateError。

**示例 1:** 此示例显示了聚合错误的捕获。

## java 描述语言

```
<script>
Promise.any([
    Promise.reject(
      new Error(
        "There is any error occured"
      )
    ),
  ]).catch(n => {

    // Check if AggregateError
    console.log(
      n instanceof AggregateError
    );

    // Print the message of the error
    console.log(n.message);

    // Print the name of the error
    console.log(n.name);

    // Print all the errors that this
    // error comprises
    console.log(n.errors);
  }
);</script>
```

**输出:**

```
true
All promises were rejected
AggregateError
[Error: There is any error occured]
```

**示例 2:** 此示例显示了聚合错误的创建。

## java 描述语言

```
<script>
try {
    throw new AggregateError([
      new Error(
        "This is Error 1"
      ),
      new Error(
        "This is Error 2"
      ),
      new Error(
        "This is Error 3"
      ),
    ], 'These are multiple errors');
  } catch (n) {

      // Check if AggregateError
      console.log(
        n instanceof AggregateError
      );

      // Print the message of the error
      console.log(n.message);

      // Print the name of the error
      console.log(n.name);

      // Print all the errors that this
      // error comprises
      console.log(n.errors);
  }
</script>
```

**输出:**

```
true
These are multiple errors
AggregateError
[Error: This is Error 1, 
 Error: This is Error 2, 
 Error: This is Error 3]

```