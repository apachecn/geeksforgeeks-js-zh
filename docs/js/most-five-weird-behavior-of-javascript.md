# JavaScript 最怪异的 5 种行为

> 原文:[https://www . geesforgeks . org/most-5-行为怪异的 javascript/](https://www.geeksforgeeks.org/most-five-weird-behavior-of-javascript/)

在本文中，我们将讨论 [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) 的怪异事实。JavaScript 以其被广泛接受而闻名，也以其怪异而闻名。下面给出的例子可以让来自 C++、Java、C#和其他语言的开发人员大吃一惊。JavaScript 是一种面向对象的编程语言，但是类的概念是在 ES6 中引入的。您可以用 JavaScript 编写 HTML 注释，min 大于 max，这里将介绍 JavaScript 的更多奇怪之处。

**1。JavaScript 中的 HTML 注释:**你可以用 JavaScript 编写 HTML 注释来验证它们的有效性。可以用 HTML 标签<！––>在您的 JavaScript 代码中没有任何错误，因为这些注释被视为 JavaScript 注释的//。这些注释用于不理解 JavaScript 的旧浏览器的<脚本>标签中。

*   **Example:**

    ## java 描述语言

    ```
    <script>
      console.log("Hello world");
      <!-- console.log('Hello World') -->
    </script>
    ```

    **输出:**

    ```
    Hello world
    ```

**2。最小大于最大:**[数学最小()](https://www.geeksforgeeks.org/javascript-math-min-method/)大于[数学最大()](https://www.geeksforgeeks.org/javascript-math-max-method/)

*   **Example 1:**

    ## java 描述语言

    ```
    <script>
      var a = Math.max() < Math.min();
      var b = Math.max() > Math.min();

      console.log(a);
      console.log(b);
    </script>
    ```

    **输出:**

    ```
    true
    false
    ```

*   **例 2:** 还有一点是 Math.max()返回-Infinity，Math.min()返回 Infinity

    ## java 描述语言

    ```
    <script>
      var a = Math.max();
      var b = Math.min();

      console.log(a);
      console.log(b);
    </script>
    ```

    **输出:**

    ```
    -Infinity
    Infinity
    ```

**3。在 JavaScript 中真+真+真== 3** 可以看到真+真+真等于 3。

*   **示例 1:** 这返回 3，因为当我们添加两个布尔值(真或假)时，它们会自动转换为数字。在这个例子中，真被转换成数字，当我们把真转换成数字时，我们得到 1，当我们把假转换成数字时，我们得到 0。

    ## java 描述语言

    ```
    <script>
      var a = true + true + true;

      console.log(a);
    </script>
    ```

    **输出:**所以真+真+真变成了 1 + 1 + 1，因此我们得到了结果 3。

*   **Example 2:**

    ## java 描述语言

    ```
    <script>
      let a = Number(true);
      let b = Number(false);

      console.log(a);
      console.log(b);
    </script>
    ```

    **输出:**

    ```
    1
    0
    ```

*   **例 3:** 下面是一些与本例相关的有趣结果。

    ## java 描述语言

    ```
    <script>
      var a = true + true;
      var b = true + false;
      var c = false + false;
      var d = 2 * true;
      var e = 2 * false;

      var f = (true + true) * (true + true) - true;
      console.log(a, b, c, d, e, f);
    </script>
    ```

    **输出:**

    ```
    2
    1
    0
    2
    0
    3
    ```

**4。 [NaN](https://www.geeksforgeeks.org/javascript-number-nan-property/) 不是 NaN:** NaN 不等于 NaN 即使我们使用严格相等运算符(= = = =)。

*   **Example:**

    ## java 描述语言

    ```
    <script>
      var a = NaN;
      var b = NaN;

      console.log(a == b);
      console.log(a === b);
    </script>
    ```

    **输出:**

    ```
    false
    false
    ```

**5。真真假假:**当我们应用两个后比较字符串真和字符串假的时候！接线员，然后我们得到真实的。

*   **Example 1:** When we apply two logical not operator, we get true.

    ## java 描述语言

    ```
    <script>
      console.log(!!"true" == !! "false");
      console.log(!!"true" === !! "false");
      console.log(!!"Hello" == !! "world");
    </script>
    ```

    **输出:**

    ```
    true
    true
    true
    ```

*   **例 2:** 当我们比较真和真的时候，就得到真。

    ## java 描述语言

    ```
    <script>
      console.log(!!"Geeksforgeeks");

      console.log(!!"true");
    </script>
    ```

    **输出:**

    ```
    true

    ```