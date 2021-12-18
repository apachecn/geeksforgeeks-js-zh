# JavaScript 中的字符串插值

> 原文:[https://www . geesforgeks . org/string-interpolation-in-JavaScript/](https://www.geeksforgeeks.org/string-interpolation-in-javascript/)

字符串插值是一个很棒的编程语言特性，它允许将变量、函数调用、算术表达式直接注入到字符串中。ES6 之前的 JavaScript 中没有字符串插值。字符串插值是 ES6 的一个新特性，它可以在不需要转义字符的情况下生成多行字符串。我们可以很容易地使用撇号和引号，这样它们可以使我们的字符串以及代码更容易阅读。这些是在字符串连接上使用字符串插值的一些原因。

让我们看看字符串串联和字符串插值的区别。

```
<script>

// String Concatenation
function myInfo(fname, lname, country) {
    return "My name is " + fname + " " + lname + ". " 
              + country + " is my favorite country."; 
}
console.log(myInfo("john", "doe", "India"));
</script>
```

**输出:**

```
My name is john doe. India is my favorite country
```

在字符串连接中，很难维护字符串，因为它们变得越来越大，变得繁琐和复杂。为了使它可读，开发人员必须维护所有空白。这就是 ES6 用字符串插值拯救的地方。在 JavaScript 中，作为占位符的模板文字(用倒勾` `包装的字符串)和${expression}执行字符串插值。现在我们可以用字符串插值来编写上面的 myInfo 函数。

```
<script>

// String Interpolation
function myInfo(fname, lname, country) {
    return `My name is ${fname} ${lname}. ${country} is my favorite country`; 
}
console.log(myInfo("john", "doe", "India"));
</script>
```

**输出:**

```
My name is john doe. India is my favorite country
```

我们可以看到，与串联相比，代码很小，很容易阅读。模板字符串支持占位符。像变量、函数调用、算术这样的表达式可以放在占位符内。这些表达式在运行时进行计算，并将输出插入字符串中。

```
<script>

// DEclare and initialize variables
const x = "GeeksforGeeks";

// I like GeeksforGeeks
console.log(`I like ${x}.`);

// Function call
function greet() {
    return "hello!";
}

// hello! I am a student.
console.log(`${greet()} I am a student.`); 

// Expression evolution
//sum of 5 and 6 is 11. 
console.log(`sum of 5 and 6 is ${5+6}.`);

</script>
```

**输出:**

```
I like GeeksforGeeks
hello! I am a student.
sum of 5 and 6 is 11.

```

我们也可以在表达式中使用条件语句。例如:

```
<script>

function isEven(x) {
    console.log(`x is ${x%2 === 0 ? 'even' : 'odd'}`);
}

isEven(4); // x is even
</script>
```

**输出:**

```
x is even
```

字符串插值是一个很好的特性。它有助于将值插入字符串。它使代码更易读，避免了笨拙。