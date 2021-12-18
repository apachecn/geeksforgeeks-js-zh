# JavaScript 类级字段

> 原文:[https://www . geesforgeks . org/JavaScript-类级-字段/](https://www.geeksforgeeks.org/javascript-class-level-fields/)

在任何面向对象的编程语言中，类都可以有私有和公共字段。字段只是保存信息的变量。面向对象编程语言中有两种类型的字段，即实例字段和静态字段。实例成员属于特定的实例。

**示例:**如果我们创建 3 个实例(对象)，内存中将有 3 个实例字段副本，而无论我们创建多少个实例，静态字段都将只有一个副本。简单地说，静态变量是所有对象共有的变量。

**私有实例字段:**默认情况下，类的所有属性都是公共的，可以在类外修改。因此，为了声明一个私有类字段，我们需要使用#前缀。

**语法:**

```
#variableName
```

让我们看看下面的例子:

## java 描述语言

```
<script>
class IncrementCounter {

    // Private variable
    #value = 0;

    // Public variable
    Count = 0;

    Increment() {
        this.#value++;
    }
}

const counter = new IncrementCounter();

// Raises an error
console.log(counter.#value);

// Calling the increment function
counter.increment();

// Printing the private variable value
console.log(counter.#value);
</script>
```

**输出:**

> console.log(计数器。#值)；
> ^
> 语法错误:私有字段“#value”必须在 wrapSafe(内部/模块/cjs/loader.js:1054:16)
> 模块的封闭类
> 中声明。_ 编译(内部/模块/cjs/loader.js:1102:27)
> 在对象.模块. _ 扩展..js(internal/modules/cjs/loader . js:1158:10)
> at module . load(internal/modules/cjs/loader . js:986:32)
> at function . module . _ load(internal/modules/cjs/loader . js:879:14)
> at function . executeuserentrypoint[as runMain](internal/modules/run _ main . js:71:12)
> at internal/main/run _ main

**解释:**在上面的例子中，我们使用#声明了一个私有变量。运行上述脚本将显示一个错误，因为“私有字段' #value '必须在封闭类中声明”，因为我们试图访问类外的私有变量。因此，我们试图通过定义如下函数来获得该值:

## java 描述语言

```
<script>
class IncrementCounter {
    #value = 0;

    increment() {
        this.#value++;
    }

    value() {

        // Returning the value of
        // a private variable
        return this.#value;
    }
}

const counter = new IncrementCounter();

// Calling the function value()
console.log(counter.value());

// Calling the function increment()
counter.increment();

// Calling the function value()
console.log(counter.value());
</script>
```

**输出:**

```
0
1
```

**私有静态字段:**可以使用关键字 static 创建静态字段。有时甚至静态字段也保持隐藏，您可以将其设为私有。

**语法:**

```
static #staticFieldName
```

让我们看看下面的例子:

## java 描述语言

```
<script>
class User {

    // Private static field of string type
    static #name = "";

    // Private static field
    static #age

    // Constructor function
    Person(user_name, user_age) {
        User.#name = user_name;
        User.#age = user_age;
        return User.#name + ' ' + User.#age;
    }
}

// Create an object user1
user1 = new User();
console.log(user1.Person("John", 45));

// Create an object user2
user2 = new User()
console.log(user1.Person("Mark", 35));
</script>
```

**输出:**

```
John 45
Mark 35
```

**解释:**要调用静态字段，我们需要使用构造函数类的名称。在上面的例子中，我们使用关键字 static 和#为私有字段创建了一个私有静态字段名，并将其初始化为一个空字符串。同样，我们正在创建一个私有静态字段时代。现在，为了调用上面创建的字段，我们使用构造函数类 User 的名称作为 User。#名称和用户。#年龄。

**公共实例字段:**默认情况下，类的所有属性都是公共的，可以在类外轻松访问。您可以初始化变量的值以及声明。

让我们看看下面的例子:

## java 描述语言

```
<script>
class IncrementCounter {

    // Public instance field
    value = 1;

    Increment() {
        return this.value++;
    }
}

const counter = new IncrementCounter();

// Accessing a public instance field
console.log(counter.value);

// Calling the Increment function
counter.Increment();

// Printing the updated value
console.log(counter.value);
</script>
```

**输出:**

```
1
2
```

**说明:**在上面的例子中，value 被声明为公共实例并初始化为 1，所以我们可以很容易地使用 *counter.value* 来访问它。对访问和修改构造函数、方法内部以及类外部的公共实例字段没有限制。

**公共静态字段:**正如我们之前讨论过的，静态字段是通过使用 static 关键字作为 staticFieldName 来创建的。

让我们看看下面的例子:

## java 描述语言

```
<script>
class Example {

    // Private static field
    static value = 42;
}

// Accessing a public static field using
// name of the Constructor class
console.log(Example.value)

console.log(Example.value === 42);
</script>
```

**输出:**

```
42
true
```

**说明:**如您所见，我们可以通过使用类名轻松访问类外的公共静态字段。