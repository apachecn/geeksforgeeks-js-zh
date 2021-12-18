# 用 JavaScript 编写更好条件句的技巧

> 原文:[https://www . geesforgeks . org/tips-for-writing-better-conditions-in-JavaScript/](https://www.geeksforgeeks.org/tips-for-writing-better-conditionals-in-javascript/)

如果您使用的是 JavaScript，那么您将会编写大量包含大量条件的代码。起初，条件句似乎很容易学习，但它不仅仅是写一些 if-else 语句。

面向对象编程允许人们避免条件，并用多态和继承来代替它们。你应该尽可能遵循这些原则。但另一方面，由于各种原因，您可能最终会在代码中使用条件句。本文的目的是帮助您组织条件语句。

**用条件句写代码的技巧:**

1.  **Array.includes:** 可以对多个条件使用 **array.includes()** 方法。 **array.includes()** 方法用于确定数组中是否存在特定元素。它返回“真”或“假”

**示例:**下面的代码演示了，如何检查动物是“狮子”还是“狗”。

## java 描述语言

```
// function
function test(animal) {
    if (animal == 'Lion' || animal == 'dog') {
        console.log('Valid');
    }
}

// function call
test('dog');
```

**输出:**

```
Valid
```

上面的代码看起来很简单，因为你只需要检查两种动物。但是，您不确定用户的输入。如果你多养几只动物呢？如果继续用更多的*或*语句扩展语句，代码将更难维护，看起来非常不干净。

你可以重写函数，使它更干净。所有你需要做的是添加一个新的数组项目，如果你想检查一些其他的动物。

## java 描述语言

```

function test(animal) {
    const animals = ['dog', 'cat', 'cow', 'Lion'];

    // Used to check if a particular
    // element is present 
    if (animals.includes(animal)) {
        console.log('valid');
    }
}
console.log(test('dog'));
```

**输出:**

```
valid
```

您可以创建一个动物数组，将条件与代码的其余部分分开。您甚至可以将变量声明在函数范围之外，并在任何需要的地方重用它。这是一种编写易于理解和维护的干净代码的方法。

*   **Array.every & Array.some:**

    **array.every()** 方法用于检查数组中存在的所有元素是否满足给定条件。当每个数组元素满足给定条件时，它返回“真”，否则返回“假”。

    **array.some()** 方法检查数组中是否有任何元素通过了提供的函数测试。 **array.some()** 方法对数组的每个元素执行一次函数。它检查数组中是否至少有一个元素满足条件。

    这两个 JavaScript Array 函数用于减少代码行。请看下面给出的代码。

    ## java 描述语言

    ```
    // Array of objects
    const cars = [
        { name: 'car1', color: 'red' },
        { name: 'car2', color: 'blue' },
        { name: 'car3', color: 'purple' }
    ];

    function test() {
        let isAllblue = true;

        // Condition: all cars must be blue
        for (let c of cars) {
            if (!isAllblue) break;
            isAllblue = (c.color == 'blue');
        }

        console.log(isAllblue);
    }
    test();
    ```

    **输出:**

    ```
    false
    ```

    上面的代码有点长。可以使用 **Array.every()** 方法进行约简。

    ## java 描述语言

    ```
    // Array of objects
    const cars = [
        { name: 'car1', color: 'red' },
        { name: 'car2', color: 'blue' },
        { name: 'car3', color: 'purple' }
    ];

    function test() {

        // Condition: short way
        // all cars must be in blue color
        const isAllblue = cars.every(
                c => c.color == 'blue');

        console.log(isAllblue);
    }
    test();
    ```

    **输出:**

    ```
    false
    ```

    也可以使用 **Array.some()** 方法实现

    ## java 描述语言

    ```
    // Array of objects
    const cars = [
        { name: 'car1', color: 'red' },
        { name: 'car2', color: 'blue' },
        { name: 'car3', color: 'purple' }
    ];

    function test1() {

      // Condition: if any car is in blue color
      const isAnyblue = cars.some(c => c.color == 'blue');

      console.log(isAnyblue); 
    }
    test1();
    ```

    **输出:**

    ```
    true
    ```

    *   **Return Early or Early exit:** The Return Early in JavaScript is an easy way to reduce a function body to zero the number of “else” statements. There are many reasons to use Return Early in your code.
    1.  它减少了代码总量。
    2.  它通过降低逻辑复杂度来减少行的长度。
    3.  它有助于提高可读性。

    早期 return 的目的是通过在主体的“if”语句中使用“Return”关键字来消除 JavaScript 函数中对“else”条件的需要。让我们创建一个在特定条件下表现不同的函数。

    **注:**下面演示上述解释的伪代码。

    ## java 描述语言

    ```
    function IsRed(someObject) {

        // Declare a variable to 
        // store the final value
        var willRed;

        // Compare type of object
        if (typeof someObject === 'object') {

            // Check object color property
            // is red or not 
            if (someObject.color === 'Red') {
                willRed = true;
            } else {
                willRed = false;
            }
        } else {
            willRed = false;
        }

        return willRed;
    }
    ```

    这个功能很清楚，但似乎不必要的复杂。早期返回模式可以用来增加可读性，减少“else”语句的数量。

    ## java 描述语言

    ```
    // Use return instead of else statement
    function IsRed(someObject) {
        if (typeof someObject !== 'object') {
            return false;
        }

        if (someObject.color !== 'Red') {
            return false;
        }

        return true;
    }
    ```

    使用提前返回模式，我们能够消除所有不必要的“否则”语句，并使您的功能更加清晰和简洁。

    您也可以只使用一个“if”语句来重构这个函数。

    ## java 描述语言

    ```
    // Here you can reduce your code
    function IsRed(someObject) {

        // 2 if statements replaced
        // by 1 if statement
        if (
            typeof someObject !== 'object' ||
            someObject.color !== 'Red'
        ) {
            return false;
        }
        return true;
    }
    ```

    通过使用 JavaScript 的三元运算符，可以在单行代码中再次重构该函数。

    ## java 描述语言

    ```
    function IsRed(someObject) {
        return typeof someObject !== 'object'
            || someObject.color !== 'Red' ? false : true;
    }
    ```

    通过减少条件，您减少了所有嵌套的“if”语句。

    **注意:**始终以少筑巢、早归为目标，但不要糟蹋它。如果你的代码简短直接，如果嵌套的“如果”更清晰。

    *   **Use Object Literal or Maps:** The object literal is basically an array of key:value pairs which are used instead of switch statements. Let us look at the example below.

    ## java 描述语言

    ```
    function printCars(color) {

        // Use switch case to 
        // find cars by color
        switch (color) {
            case 'red':
                return ['Rcar1', 'Rcar2'];
            case 'blue':
                return ['Bcar1', 'Bcar2'];
            case 'purple':
                return ['Pcar1', 'Pcar2'];
            default:
                return [];
        }
    }

    printCars(null);
    printCars('blue');    
    ```

    **输出:**

    ```
     []
    ['Bcar1', 'Bcar2']

    ```

    上述代码可以通过使用对象文字并完全替换“switch”语句来重构。

    ## java 描述语言

    ```
    // Use object literal to 
    // find cars by color
    const carColor = {
        red: ['Rcar1', 'Rcar2'],
        blue: ['Bcar1', 'Bcar2'],
        purple: ['Pcar1', 'Pcar2']
    };

    function printcars(color) {
        return carColor[color] || [];
    }
    console.log(printcars());
    console.log(printcars('red'));
    console.log(printcars('blue')); 
    ```