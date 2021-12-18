# JavaScript 中的析构赋值

> 原文:[https://www . geesforgeks . org/destruction-赋值 in-javascript/](https://www.geeksforgeeks.org/destructuring-assignment-in-javascript/)

析构赋值是一个 JavaScript 表达式，允许**将数组中的值**或对象中的属性解包为不同的变量。数据可以从*数组、对象、嵌套对象*和**中提取，并赋值给变量**。在析构赋值中，左侧定义了应该从源变量中解包哪个值。

一般来说*提取*的数组的实现方式如下所示:
**例:**

```
<script>
var names = ["alpha", "beta", "gamma", "delta"];

var firstName = names[0];
var secondName = names[1];

console.log(firstName);//"alpha"
console.log(secondName);//"beta"
</script>
```

**输出:**

```
alpha
beta
```

**语法:**

*   **Array destructuring:**

    ```
    var x, y;
    [x, y] = [10, 20];
    console.log(x); // 10
    console.log(y); // 20
    ```

    或者

    ```
    [x, y, ...restof] = [10, 20, 30, 40, 50];
    console.log(x); // 10
    console.log(y); // 20
    console.log(restof); // [30, 40, 50]
    ```

*   **Object destructuring:**

    ```
    ({ x, y} = { x: 10, y: 20 });
    console.log(x); // 10
    console.log(y); // 20
    ```

    或者

    ```
    ({x, y, ...restof} = {x: 10, y: 20, m: 30, n: 40});
    console.log(x); // 10
    console.log(y); // 20
    console.log(restof); // {m: 30, n: 40}
    ```

**数组析构:**利用 JavaScript 数组中的析构赋值可能出现的情况，下面列出了所有的例子:

*   **Example 1:** When using **destructuring assignment** the same extraction can be done using below implementations.

    ```
    <script>
    var names = ["alpha", "beta", "gamma", "delta"];
    var [firstName, secondName] = names;

    console.log(firstName);//"alpha"
    console.log(secondName);//"beta"

    //Both of the procedure are same
    var [firstName, secondName] = ["alpha", "beta", "gamma", "delta"];

    console.log(firstName);//"alpha"
    console.log(secondName);//"beta
    </script>
    ```

    **输出:**

    ```
    alpha
    beta
    alpha
    beta
    ```

*   **Example 2:** The array *elements* can be *skipped* as well using a *comma* separator. A single comma can be used to skip a single array element. One key difference between the **spread operator** and array destructuring is that the spread operator unpacks all array elements into a comma-separated list which does not allow us to pick or choose which elements we want to assign to variables. To skip the whole array it can be done using the number of commas as there is a number of array elements.

    ```
    <script>
    var [firstName,,thirdName] = ["alpha", "beta", "gamma", "delta"];

    console.log(firstName);//"alpha"
    console.log(thirdName);//"gamma"
    </script>
    ```

    **输出:**

    ```
    alpha
    gamma
    ```

*   **Example 3:** In order to assign some array elements to variable and rest of the array elements to only a single variable can be achieved by using **rest operator (…)** as in below implementation. But one limitation of rest operator is that it works correctly only with the last elements implying a subarray cannot be obtained leaving the last element in the array.

    ```
    <script>
    var [firstName,,...lastName] = ["alpha", "beta", "gamma", "delta"];

    console.log(firstName);//"alpha"
    console.log(lastName);//"gamma, delta"
    </script>
    ```

    **输出:**

    ```
    alpha
      0: "gamma"
      1: "delta"

    ```

*   **Example 4:** Values can also be **swapped** using destructuring assignment as below:

    ```
    <script>
    var names = ["alpha", "beta", "gamma", "delta"];

    console.log(firstName);//"alpha"
    console.log(secondName);//"beta"

    //After swapping
    [firstName, secondName] = [secondName, firstName]

    console.log(firstName);//"beta"
    console.log(secondName);//"alpha"
    </script>
    ```

    **输出:**

    ```
    beta
    alpha

    ```

*   **Example 5:** Data can also be extracted from an array returned from a function. One advantage of using a destructuring assignment is that there is no need to manipulate an entire object in a function but just the fields that are required can be copied inside the function.

    ```
    <script>
    function NamesList() {
            return ["alpha", "beta", "gamma", "delta"]
        }
    var[firstName, secondName] = NamesList();

    console.log(firstName);//"alpha"
    console.log(secondName);//"beta"
    </script>
    ```

    **输出:**

    ```
    alpha
    beta
    ```

*   **Example 6:** In *ES5* to **assign variables from objects** its implementation is

    ```
    <script>
    var marks = {x: 21, y: -34, z: 47 };

    var x = marks.x; // x = 21
    var y = marks.y; // y = -34
    var z = marks.z; // z = 47

    console.log(x);
    console.log(y);
    console.log(z);
    </script>
    ```

    **输出:**

    ```
    21
    -34
    47
    ```

*   **Example 7:** The above implementation in *ES6* using destructuring assignment is.

    ```
    <script> 
    var marks = {x: 21, y: -34, z: 47 }; 

    const { x, y, z } = marks; // x = 21, y = -34, z = 47 

    console.log(x); 
    console.log(y); 
    console.log(z); 
    </script> 
    ```

    **输出:**

    ```
    21
    -34
    47
    ```

**物体破坏:**

*   **Example:** The *Nested objects* can also be destructured using destructuring syntax.

    ```
    <script>
    const marks = {
      section1: { alpha: 15, beta: 16},
      section2: { alpha: -31, beta: 19 }
    };
    const { section1 : { alpha: alpha1, beta: beta1 }} = marks;
    console.log(alpha1, beta1); // 15, 16

    </script>
    ```

    **输出:**

    ```
    15 16

    ```