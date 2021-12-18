# JavaScript | For 循环

> 原文:[https://www.geeksforgeeks.org/javascript-for-loop/](https://www.geeksforgeeks.org/javascript-for-loop/)

编程语言中的循环是一种便于重复执行一组指令，直到某个条件评估为假的特性。我们遇到了循环的**，它提供了一种编写循环结构的简单而系统的方法。**

**语法:**

```
for (statement 1 ; statement 2 ; statement 3)

```

*   **语句 1** 是计数器的初始化。它在代码块执行之前执行一次。
*   **语句 2** 是定义代码块执行条件的测试语句，它必须返回一个布尔值。它也是一个入口控制的循环，因为在执行循环语句之前会检查条件。
*   **语句 3** 是在代码块执行后(每次)执行的计数器&的增量或减量。

```
<script type = "text/javaScript"> 
// JavaScript program to illustrate for loop
    var x; 

    // for loop begins when x=2 
    // and runs till x <=4 
    for (x = 2; x <= 4; x++)  
    { 
        document.write("Value of x:" + x + "<br />"); 
    } 

< /script> 
```

**输出:**

```
Value of x:2
Value of x:3
Value of x:4

```

流程图:
![](img/755ce1820070a39c0aad74a21558f9b8.png)

**语句 1**
我们可以从外部而不是在语句 1 中初始化计数器变量。这清楚地向我们表明，语句 1 是可选的。我们可以用分号将该部分留空。例如:

```
<script>
    var x = 2; 

    for ( ; x <= 4; x++)  
    { 
        document.write("Value of x:" + x + "<br />"); 
    }  
</script>
```

**语句 2**
该语句检查测试条件的布尔值。如果测试条件为真，for 循环将进一步执行。每当 for 循环在循环进入其主体之前运行时，都会执行它。如果此语句返回 true，循环将重新开始，否则它将结束并移到循环体后面的代码。这也是一个可选语句，如果留空，Javascript 会将其视为真。如果省略此语句，如果循环控件没有被手动中断，循环将无限期运行。这解释如下:

```
<script>
 var x = 2; 
 bool 
    for ( ; ; x++)  
    { 
        document.write("Value of x:" + x + "<br />"); 
        break;
    }  
</script>
```

**语句 3**
是控制计数器变量的递增/递减的受控语句。它本质上也是可选的，可以在循环体内完成。例如:-

```
<script>
var i = 0;
var len = 2;
var gfg = "";
for (; i < len; ) { 
  gfg += cars[i] + "<br>";
//can be increased inside loop
  i++;
}
</script>
```

#### 为/在

在循环中，还有另一个名为**的高级循环，它贯穿对象的所有属性。该循环将对对象的每个属性执行一次。**

```
Syntax : for (var in object) { statements to be executed } 
```

**示例:**

```
<!DOCTYPE html>
<html>
<body style = "text-align:center;"> 

<h1 style = "color:green;" > 
GeeksForGeeks 
</h1> 

<button onclick="GFG()">Try it</button>

<p id="demo"></p>

<script>
function GFG() {
  var Platform= {fname:"geeks", Mname:"for", lname:"geeks", }; 

  var text = "";
  var x;
  for (x in Platform) {
    text += Platform[x] + " ";
  }
  document.getElementById("demo").innerHTML = text;
}
</script>

</body>
</html>
```

**输出:**
![](img/8e89dfcd166e0040bc2ed46aa4fb19bc.png)