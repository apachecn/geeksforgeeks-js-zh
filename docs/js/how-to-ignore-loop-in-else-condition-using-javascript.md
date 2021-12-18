# 如何用 JavaScript 忽略 else 条件下的循环？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 忽略其他条件循环/](https://www.geeksforgeeks.org/how-to-ignore-loop-in-else-condition-using-javascript/)

在其他情况下有两种方法可以忽略循环:

*   **继续**
*   **断开**

相同的解释见[本](https://www.geeksforgeeks.org/break-continue-and-pass-in-python/)。
简单来说， **Break** 语句退出循环，而 **continue** 语句退出特定迭代。

让我们用一些例子来进一步理解。

**对于带有继续语句的循环:**

```
// Defining the variable
var i;

// For loop 
for (i = 0; i < 3; i++) {

    // If i is equal to 1, it
    // skips the iteration
    if (i === 1) { continue; }

    // Printing i
    console.log(i);
}
```

**输出:**

```
0
2
```

**带中断语句的循环:**

```
// Defining the variable
var i;

// For loop 
for (i = 0; i < 3; i++) {

    // If i is equal to 1, it comes
    // out of the for a loop
    if (i === 1) { break; }

    // Printing i
    console.log(i);
}
```

**输出:**

```
0
```

**对于每个循环:**当涉及到 forEach 循环时，AngularJS 会因为 break 和 continue 语句而变得非常混乱。

break 和 continue 语句不能像预期的那样工作，实现 continue 的最好方法是使用 return 语句，break 不能在 forEach 循环中实现。

```
// Loop which runs through the array [0, 1, 2]
// and ignores when the element is 1
angular.forEach([0, 1, 2], function(count){
    if(count == 1) {
        return true;
    }

    // Printing the element
    console.log(count);
});
```

**输出:**

```
0
2
```

但是，可以通过包含布尔函数来实现中断操作，如下例所示:

```
// A Boolean variable
var flag = true;

// forEach loop which iterates through
// the array [0, 1, 2]
angular.forEach([0, 1, 2], function(count){

    // If the count equals 1 we
    // set the flag to false
    if(count==1) {
        flag = false;
    }

    // If the flag is true we print the count
    if(flag){ console.log(count); }
});
```

**输出:**

```
0
```