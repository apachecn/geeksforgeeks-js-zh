# TypeScript 中的“string”和“String”有什么区别？

> 原文:[https://www . geesforgeks . org/string 和 string-in-typescript 的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-string-and-string-in-typescript/)

与 JavaScript 不同，TypeScript 使用静态类型，即它指定变量能够保存哪种数据。因为 TypeScript 是 JavaScript 的上标，所以它也区分了字符串和字符串。JS 中字符串对象的使用非常少。字符串对象具有向对象添加属性的特性。

一般来说，字符串(带小“S”)表示一个原语，而字符串(带大写“S”)表示一个对象。JavaScript 支持五种类型的原语，string 就是其中之一。您将从链接的文章中获得 JavaScript 中[变量和数据类型的概念。](https://www.geeksforgeeks.org/variables-datatypes-javascript/)

**基元字符串:**字符串(带一个小的' s ')表示一个基元，基元是没有属性的值。字符串文字和从字符串函数调用返回的一些字符串可以归类为一个原语(字符串)。可以使用包装器将基本字符串转换为对象。

**语法:**

```
var test1 = "A TypeScript variable of type 'string'";
```

**对象字符串:**对象是不同属性的累积。一个对象可以调用许多与之对应的方法。

**语法:**

```
var test2 = new String('another test');
```

*   **示例:**

## java 描述语言

```
<script>
let a = new String("An object !");
let b = "A literal ! haha";
console.log(typeof(a));
console.log(typeof(b));
</script>
```

**输出:**

```
object 
string 
```

在上面的代码中，我们看到变量“a”的类型是一个对象，而“b”是一个原语(字符串)。它表明字符串文字是原始的。这里需要注意的重要一点是，我们能够对“b”使用方法，即使它不是一个对象。这是因为当一个方法通过它被调用时，JavaScript 会将一个原语更改为它的对象。这种情况发生的时间非常短，只是为了执行方法并返回到原始状态。那么为什么问题可能会到来，为什么我们需要字符串对象！

**需要字符串对象:**
当我们使用关键字 new 时，TS 每次都会创建一个新的对象，这与使用基元类型时不同，如果变量具有相同的值，那么它们会指向相同的内存。参考下面的例子。

*   **示例 1:** 下面的示例将显示 a1 和 b1 是如何被显示为相等的，因为它们是具有相同值的文字，而 a2 和 b2 被显示为不同的，因为我们使用了关键字 new 来创建两个不同的对象。

## java 描述语言

```
<script>
let a1 = "Hello World";
let b1 = "Hello World";
console.log(a1 != b1);
let a2 = new String("Hello World");
let b2 = new String("Hello World");
console.log(a2 != b2);
</script>
```

**输出:**

```
false
true
```

*   **示例 2:**eval 的使用因基元字符串和对象而异。请参考以下示例。在本例中，我们将看到使用 [**eval()方法**](https://www.geeksforgeeks.org/javascript-eval-function/) 时，字符串和 string 有何不同。字符串基元被直接求值，即 25 * 25 给出 525 作为输出，而对象将给出输出本身，因为如果 eval()不是基元字符串，它返回的参数不变。我们也可以使用 [**toString()方法**](https://www.geeksforgeeks.org/javascript-tostring-function/) 将对象更改为原始字符串来评估对象。

## java 描述语言

```
<script>
var a3 = '21 * 25' ;
console.log(eval(a3));
var b3 = new String("1 + 1");
console.log(eval(b3));
console.log(eval(b3.toString()));
</script>
```

**输出:**

```
525 
String { "1 + 1" }
2
```

如上所述，字符串对象可以保存属性。我们可以使用字符串对象来保存属性中的附加值。尽管这并不常用，但它仍然是 JS 的一个特性。

```
var primitive = 'hello';
var object = new String('HELLO');
primitive.prop = 'world';//Invalid
object.prop = 'WORLD';//Valid
```

**字符串与字符串的区别:**

<figure class="table">

| String primitive | String object |
| --- | --- |
| String primitives are widely used. | String objects are rarely used. |
| String primitives only hold values. | A string has the ability to hold properties. |
| String is immutable, so it is thread safe. | String objects are mutable. |
| This string primitive has no method. | String objects have methods. |
| You cannot create two different words with the same value. | You can create a new object with the keyword' new'. |
| It is a primitive data type. | Wrap raw data types to create objects. |
| By value transfer, that is, the copy entity itself is transferred. | Pass with reference to actual data. |
| When using eval (), these are directly treated as source code. | When using eval (), these are treated as strings. |

</figure>