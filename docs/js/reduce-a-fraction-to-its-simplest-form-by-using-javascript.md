# 用 JavaScript 把分数简化成最简单的形式

> 原文:[https://www . geesforgeks . org/通过使用 javascript 将分数简化为最简单的形式/](https://www.geeksforgeeks.org/reduce-a-fraction-to-its-simplest-form-by-using-javascript/)

如果分子和分母之间没有共同的因子(除了 1)，分数就被简化了。例如，4/6 不是简化的，因为 4 和 6 都共享 2 作为因子。如果不恰当的分数可以转化为整数。有两种可能的方法可以通过使用 JavaScript 来简化分数。

*   使用 math.js 简化()函数
*   使用 [JavaScript _。减少()功能](https://www.geeksforgeeks.org/javascript-_-reduce-with-examples/)

下面的例子将说明这种方法:

**使用 math.js simplify()函数:**在该函数中，表达式上应用了很少的规则，您可以创建自己定制的规则。基本上这个函数就像 lambda 函数。在那里你可以根据自己的要求制定规则。

*   **例:**

    ```
    Input :simplify("4/6") 
    Output :"2/3"
    ```

*   **程序:**

    ```
    <script type = "text/javaScript">

    // main function
    function simplify(str) {
        var result = '', data = str.split('/'), 
            numOne = Number(data[0]), 
            numTwo = Number(data[1]);
        for (var i = Math.max(numOne, numTwo); i > 1; i--) {
        if ((numOne % i == 0) && (numTwo % i == 0)) {
            numOne /= i;
            numTwo /= i;
        }
        }
        if (numTwo === 1) {
        result = numOne.toString()
        } else {
        result = numOne.toString() + '/' + numTwo.toString()
        }
        return result
    }
    document.write(simplify("4/6") + "<br>");

    document.write(simplify(84810,985612));

    </script>                    
    ```

*   **输出:**

    ```
    2/3
    42405/492806
    ```

**使用 JavaScript _。reduce()函数:** The _。reduce()是 JavaScript 中的一个内置函数，用于将数组/对象的属性转换为单个值，或者用于从给定的值列表中创建单个结果。当列表中的所有元素都被传递给函数/iterate 并且没有剩余的元素时，那么 _。每个循环结束。在这里，我们将找到这些数字的 GCD，并将其除以 GCD，我们可以使输出更简单。

*   **例:**

    ```
    Input: 15, 20
    Output: 3,4
    ```

*   **程序:**

    ```
    <script type = "text/javaScript">

    // Simplified fraction by finding the GCD and dividing by it.
    function reduce(numer,denomin){
      var gcd = function gcd(a,b){
        return b ? gcd(b, a%b) : a;
      };
      gcd = gcd(numer,denomin);
      return [numer/gcd, denomin/gcd];
    }

    document.write(reduce(15,20) + "<br>");

    document.write(reduce(84810,985612));
    </script>                    
    ```

*   **输出:**

    ```
    3,4
    42405,492806
    ```