# 如何对照谓词函数测试一个值 x，并在 JavaScript 中返回 fn(x)或 x？

> 原文:[https://www . geesforgeks . org/how-test-a-value-x-对抗谓词-function-and-returns-fnx-or-x-in-JavaScript/](https://www.geeksforgeeks.org/how-to-test-a-value-x-against-predicate-function-and-returns-fnx-or-x-in-javascript/)

给定值 x，任务是对照谓词函数检查该值。如果值满足条件或谓词，则返回 fn(x)，否则返回 x。

谓词函数是将一个项作为输入并根据该项是否满足该条件返回 true 或 false 的函数。

**示例 1:** 在本例中，我们给了一个数字和一个条件，如果条件为真，则返回 fn(数字)，否则返回简单的数字值。

```
Condition : isEven 
Input : 6
Output : 720 

Explanation : Here condition is number that should 
              be even because our input data is 
              even so it returns the fn(6) value.
```

**代码实现:**

## java 描述语言

```
<script>

    // Function that we have to return
    function fn(x) {
        let fact = 1;
        for (i = 1; i <= x; i++) {
            fact *= i;
        }

        return fact;
    }

    // Predicate function checking even value
    function isEven(x) {
        return (x % 2 === 0);
    }

    // Function returning fn(x) if predicate
    // function return true else return x
    function test(x) {
        let e = isEven(x);

        if (e) {
            return fn(x);

        } else
            return x;
    }

    // Printing return value
    let ans = test(6);
    console.log(`This function returns ${ans}`);
</script>
```

**输出:**

```
This function returns 720
```

**示例 2:** 在本例中，我们给出了一个数字和一个测试条件，如果条件为真，则返回 fn(数字)，否则只返回数字值。

```
Condition : x less than max_value
Input : 15 
Output : 610
```

**代码实现:**

## Javascript

```
<script>

    // Initializing the max_Iteger
    let max_Iteger = 20;

    // Function we have to return
    function fn(x) {
        var b = 0;
        var a = 1;
        var sum;
        for (i = 0; i < x - 1; i++) {
            sum = a + b;
            b = a;
            a = sum;
        }
        return a;
    }

    // Predicate function checking value
    // is less than max_Iteger
    function isless(x) {
        return (x < max_Iteger);
    }

    // Function return fn(x) if predicate
    // function return true else return x
    function test(x) {
        let e = isless(x);

        if (e) {
            return fn(x);

        } else
            return x;
    }

    // Printing return value
    let ans = test(15);
    console.log(`This function returns ${ans}`);
</script>
```

**输出:**

```
The function returns 610
```

**示例 3:** 在本例中，我们给出了一个数字和一个测试条件，如果条件为真，则返回 fn(数字)，否则只返回数字值。

```
Condition : x is multiple of 3
Input : 6
Output : 7776
```

**代码实现:**

## Javascript

```
<script>

    // Function we have to return
    function fn(x) {

        let j = 1;
        for (i = 0; i < x - 1; i++) {
            j = j * x;
        }
        return j;
    }

    // Predicate function checking
    // multiple of 3
    function ismultiple(x) {
        return (x % 3 == 0);
    }

    // Function that returns fn(x) if
    // predicate function return true
    // else return false
    function test(x) {
        let e = ismultiple(x);

        if (e) {
            return fn(x);

        } else
            return x;
    }

    // Printing value
    let ans = test(6);
    console.log(`This function returns ${ans}`);
</script>
```

**输出:**

```
This function returns 7776
```