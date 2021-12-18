# JavaScript 课程| JavaScript 中的条件运算符

> 原文:[https://www . geesforgeks . org/JavaScript-course-conditional-operator-in-JavaScript/](https://www.geeksforgeeks.org/javascript-course-conditional-operator-in-javascript/)

**前题:** [JavaScript 教程| JavaScript 中的逻辑运算符](https://www.geeksforgeeks.org/javascript-course-logical-operators-in-javascript/)

**条件运算符**允许我们根据不同的条件执行不同类型的操作。我们使用“如果”语句。

```
if(expression){
   do this;
}

```

上面名为“表达式”的参数基本上是我们传递到“if”中的一个条件，如果它返回“true”，那么它里面的代码块将被执行，否则不会被执行。
**例:**

```
<script>
// if example
let age = 20;
if(age == 20){
  alert('Hola!'); // Hola!
}
</script>
```

**输出:**

```
Hola!

```

上面的代码非常简单地演示了如果条件运算符，如果我们将 age 的值更改为“20”以外的值，则什么也不会打印。

**如果如何起作用**
如果(..')'语句计算括号内的表达式，然后将其转换为布尔值。如果该布尔值为“假”，则不会打印输出。

```
if(0){
console.log('hey'); // will not be printed
}

```

```
if(1){
console.log('Yo')// Yo
}

```

**else 子句**
当 if 括号内的条件失效时，else 子句执行。

```
if(this is true){
  do this;
}else{
  do this;
}

```

**示例:**

```
<script>
// else example
let age = 21;
if(age == 20){
  alert('You are 20'); // not executed
}else{
  alert('Adios!'); // will be alerted 
}
</script>
```

**输出:**

```
Adios!

```

在某些情况下，我们可能不止有两个条件，在这种情况下，我们使用**‘else-if’**子句，该子句的括号中需要一个条件。

```
if(expression){
  do this;
}else if(expression){
  do this;
}else{
  do this;
}

```

**示例:**

```
<script>
// else-if example
let age = 22;
if(age < 18 ){
  alert('Too Young.');
}else if( age > 18 && age < 60){
  alert('Yo..bienvenido.'); // Yo..bienvenido.
}else{
  alert('adios..señor');
}
</script>
```

**输出:**

```
Yo..bienvenido.

```

**三元运算符**
在 Javascript 中，我们还有一个三元运算符，这是一种基于条件执行操作的非常简单的方法。

```
let result = condition ? value1 : value2;

```

它的工作原理类似于 if-else，基于一个条件，我们对结果进行评估。在上面的代码片段中，如果“条件”演变为“真”，则“值 1”将被执行，否则“值 2”将被执行。
**例:**

```
<script>
// ternany operator example
let age = 20;
let result = age>18 ? 'Great' : 'Not so great';
alert(result); // Great
</script>
```

**输出:**

```
Great

```

**下一个话题:** [JavaScript 课程| Javascript 提示示例](https://www.geeksforgeeks.org/javascript-course-javascript-prompt-example/)