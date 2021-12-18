# JavaScript |对象构造器

> 原文:[https://www . geesforgeks . org/JavaScript-object-constructors/](https://www.geeksforgeeks.org/javascript-object-constructors/)

**对象:**对象是以**键**形式的相关数据或功能的集合。这些功能通常由几个函数和变量组成。除了原语，所有的 JavaScript 值都是对象。

**示例:**

```
var GFG = {
    subject : "programming",
    language : "JavaScript",
}
```

这里*主题*和*语言*是**键**和*编程*和 *JavaScript* 是**值**。

**类:**在 JavaScript 中，类是一种函数。这个类类似于普通的 java 类。像其他面向对象语言一样，这些类是用**类**关键字声明的。类语法有两个组成部分:*类声明*和*类表达式*。

*   **Class declarations:**

    ```
    class GFG {
        constructor(A, B, C) {
            this.g = A;
            this.f = B;
            this.gg = C;
        }
    }
    ```

    这里的班名是 *GFG* 。

*   **Class expressions:**

    ```
    <script>
    class GFG {
        constructor(A, B) {

            // "this" refers to the address
            // of the keys "g" and "f"
            this.g = A;
            this.f = B;
        }
        print() {
            document.write(this.g +"<br>"+this.f);
        }
    }

    let gg = new GFG("JavaScript", "Java");

    gg.print();

    </script>
    ```

    **输出:**

    ```
    JavaScript
    Java
    ```

**这个关键字:**这个**这个**关键字指的是它所属的对象，像 OOPs 语言 C++、C#、JAVA 等。**这个**关键词在不同地区有不同的用法。在 JavaScript 中执行一个函数时，如果该函数引用了当前的执行上下文，那么这个引用就是调用函数或数据成员的引用。参见前面的示例。

**向对象添加属性:**可以使用**点(。)**运算符或**方括号。**，

```
var GFG = {
    articles: 'computer science',
    quantity: 3000,
};
```

**GFG** 有“文章”和“数量”两个属性。现在我们希望增加一个名为**主题**的物业名称。

*   使用点(。)操作员

    ```
    GFG.subject: 'JavaScript';
    ```

*   使用方括号:

    ```
    GFG['subject']: 'JavaScript';
    ```

这里**主语**是属性，**【JavaScript】**是属性的值。

**向构造函数添加属性:**我们不能像向对象添加属性那样向现有构造函数添加属性(参见上一点)，因为要添加属性，我们需要在构造函数下声明。

```
function GFG(a, b, c) {
    this.A = a;
    this.B = b;
    this.C = c;
    this.G = "GEEK";
}
```

在这里，我们添加一个属性名 **G** 带值**【极客】**，在这种情况下值**【极客】**不作为参数传递。

**向对象添加方法:**我们可以向现有对象添加新方法。

```
GFG.n = function () {
    return this.A + this.B;
};
```

这里的对象是 GFG。

**向构造函数添加方法:**

```
function GFG(a, b, c) {
    this.A = a;
    this.B = b;
    this.C = c;
    this.n = function () {
        return this.A + this.B;
    }
}
```

这里，在最后一行，一个方法被添加到一个对象。

**构造函数:**一个**构造函数**是初始化一个对象的函数。在 javaScript 中，构造函数更类似于普通的 Java 构造函数。

**对象构造函数:**在 JavaScript 中，有一个特殊的构造函数叫做 **Object()** 用来创建和初始化一个对象。**对象()**构造函数的返回值被赋给一个变量。该变量包含对新对象的引用。我们需要一个对象构造器来创建一个对象*“类型”*，它可以多次使用，而不必每次都重新定义对象。

**示例:**

```
function GFG(A, B, C) {
    this.g = A;
    this.f = B;
    this.gg = C;
}
```

这里， *GFG* 是构造函数名，A、B、C 是构造函数的自变量。

**实例化对象构造函数:**实例化对象构造函数有两种方式，

```
1\. var object_name = new Object(); or  
   var object_name = new Object("java", "JavaScript", "C#");
2\. var object_name = { };
```

在第一种方法中，对象是使用 **new** 关键字创建的，就像普通的 OOP 语言一样，**“Java”、“JavaScript”、“c#”**是参数，在调用构造函数时传递。
在第二种方法中，使用 ***大括号“{ }”***创建对象。

**给对象分配属性:**给对象分配属性有两种方式。

*   使用点(。)操作员

    ```
    object_name . properties = value;
    ```

*   使用第三个括号:

    ```
    object_name [ 'properties'] = value;
    ```

**示例 1:** 该示例显示了通过使用**新的**关键字并使用**点(。)**操作员。

```
<script>

    // creating object using "new" keyword
    var gfg = new Object();

    // Assigning properties to the object
    // by using dot (.) operator    
    gfg.a = "JavaScript"; 
    gfg.b = "GeeksforGeeks";

    document.write("Subject: " + gfg.a + "<br>");
    document.write("Author: " + gfg.b );
</script>                    
```

**输出:**

```
Subject: JavaScript
Author: GeeksforGeeks
```

**示例 2:** 本示例显示使用**大括号**创建对象，并使用**第三个括号“【】”**运算符为对象分配属性。

```

<script>

    // Creating an object using "{ }" bracket
    var gfg = { };

    // Assigning properties to the object 
    // by using third bracket
    gfg['a'] = "JavaScript"; 
    gfg['b']= "GeeksforGeeks";

    document.write("Subject: " + gfg.a + "<br>");
    document.write("Author: " + gfg.b );
</script>
```

**输出:**

```
Subject: JavaScript
Author: GeeksforGeeks
```

**示例 3:** 这个示例展示了如何将 function()与对象构造函数一起使用。

```
<script>

    // Creating object    
    var gfg = new Object();

    // Assigning properties to the object    
    gfg.a = "JavaScript"; 
    gfg.b = "GeeksforGeeks";

    // Use function()
    gfg.c = function () { 
        return (gfg.a +" "+ gfg.b);
    };

    document.write("Subject: " + gfg.a + "<br>");
    document.write("Author: " + gfg.b + "<br>");

    // Call function with object constructor    
    document.write("Adding the strings: "+ gfg.c() );

</script>                        
```

**输出:**

```
Subject: JavaScript
Author: GeeksforGeeks
Adding the strings: JavaScript GeeksforGeeks

```

**示例:**使用函数名创建函数的另一种方法。

```
<script>

    // Creating object using "{ }" bracket
    var gfg = { };

    // Assigning properties to the object    
    gfg.a = "JavaScript"; 
    gfg.b = "GeeksforGeeks";

    // Use function()
    gfg.c = add; 

    // Declare function add() 
    function add() { 
        return (gfg.a +" "+ gfg.b);
    };

    document.write("Subject: " + gfg.a + "<br>");
    document.write("Author: " + gfg.b + "<br>");

    // Call function with object constructor    
    document.write("Adding the strings: "+ gfg.c());

</script>                    
```

**输出:**

```
Subject: JavaScript
Author: GeeksforGeeks
Adding the strings: JavaScript GeeksforGeeks

```