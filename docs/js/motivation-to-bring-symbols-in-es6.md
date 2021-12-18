# 将符号带入 ES6 的动机

> 原文:[https://www . geesforgeks . org/动机-带来符号-in-es6/](https://www.geeksforgeeks.org/motivation-to-bring-symbols-in-es6/)

Javascript 包含六种数据类型**未定义**、**空**、**布尔**、**字符串**、**数字**和**对象**(包括数组数据类型)。**符号**是 ES6 中新引入的数据类型，也称为 JavaScript 6，这使得 JavaScript 中的数据类型总数为 7。它是一个原始数据类型，这意味着符号不能被实例化。符号是不可变的数据类型，充当对象键的唯一标识符。在引入符号之前，很难生成唯一的对象键。维护唯一的对象键很重要，以防止覆盖具有相似对象键的值，因为这可能会导致数据丢失。符号的引入有助于克服这个问题，因为不需要编写复杂的代码就可以生成唯一的密钥。使用**符号()功能**可以生成唯一的对象键。**符号()函数**返回符号类型的值。下面给出的例子说明了符号的用途。

**语法:**

```
let symbol = Symbol();
```

**示例 1:** 在本例中，我们将生成符号。

*   **代码:**

    ```
    <script>

        // Write Javascript code here
        let sym1 = Symbol()
        let sym2 = Symbol('mysymbol')
        console.log('Type of sym1: ', typeof(sym1))
        console.log('Type of sym2: ', typeof(sym2))
    </script>
    ```

*   **输出:**

    ```
    Type of sym1:  symbol
    Type of sym2:  symbol
    ```

**示例 2:** 在本例中，我们将看到 Symbol()函数生成唯一的对象键。

*   **代码:**

    ```
    <script>

        // Write Javascript code here
        let sym1 = Symbol('mysymbol')
        let sym2 = Symbol('mysymbol')
        console.log('sym1===sym2: ', sym1===sym2)
    </script>
    ```

*   **输出:**

    ```
    sym1===sym2: false
    ```

**注意:**符号数据类型是原始数据类型，不能实例化

**有符号和无符号的比较:**让我们考虑一个例子，学生在特定考试中获得的分数列表需要维护。学生们还没有被分配到他们的学号。在这种情况下，学生的名字将被用作对象键。但是，名字相似的学生可以不止一个。这可能会导致每个学生获得的分数被覆盖，从而导致数据丢失。为了克服这个问题，可以使用符号数据类型。

*   **代码 1:** 下面的代码片段显示了不使用符号的场景。

    ```
    <script>

    // Write Javascript code here
    var marks = {}
    marks["Joe"] = 100
    marks["Ana"] = 90
    marks["Chloe"] = 95
    marks["Marie"] = 75
    console.log(marks)
    console.log('Another student with'
              + ' name Chloe appears')
    marks['Chloe'] = 60
    console.log('After the marks of the'
         + ' fifth student is entered')
    console.log(marks)
    </script>
    ```

*   **输出:**当另一个同名学生出现时，克洛伊的标记被覆盖。
    T3】
*   **代码 2:** 下面的代码片段显示了使用符号

    ```
    <script>

    // Write Javascript code here
    var marks={}
    var sym1=Symbol("Joe")
    marks[sym1]=100
    var sym2=Symbol("Ana")
    marks[sym2]=90
    var sym3=Symbol("Chloe")
    marks[sym3]=95
    var sym4=Symbol("Marie")
    marks[sym4]=75
    console.log(marks)
    console.log('Another student '
        + 'with name Chloe appears')
    var sym5=Symbol("Chloe")
    marks[sym5]=60
    console.log('After the marks of '
        + 'the fifth student is entered')
    console.log(marks)
    </script>
    ```

    的场景
*   **输出:**当出现另一个同名学生时，克洛伊的标记不会被覆盖，没有数据丢失。你必须在本地运行这个。
    T3】

**符号限制:**

*   符号在中被忽略..循环中。
*   被**[【object . keys()](https://www.geeksforgeeks.org/object-keys-javascript/)****object . getownpertynames()**和 **[JSON.stringify()](https://www.geeksforgeeks.org/javascript-json-stringify-with-examples/)** 等函数忽略，因此无法序列化。
*   符号主要用于确保隐私。但是像**object . getownpertysymbols()**这样的方法返回任何基于符号的键的数组，而 **Reflect.ownKeys()** 返回包括符号在内的所有键的数组。