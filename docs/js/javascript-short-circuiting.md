# Javascript 短路运算符

> 原文:[https://www.geeksforgeeks.org/javascript-short-circuiting/](https://www.geeksforgeeks.org/javascript-short-circuiting/)

下面是短路运算符的示例。

*   **例:**

    ```
    <script> 
        function gfg() { 
              // AND short circuit
             document.write(false && true) 
             document.write("</br>");
             document.write(true && true) 
             document.write("</br>");
              // OR short circuit
             document.write(true || false) 
             document.write("</br>");
             document.write(false || true) 
        } 
        gfg(); 
    </script>
    ```

*   **输出:**

    ```
    false
    true
    true
    true

    ```

在 JavaScript 短路中，从左到右计算表达式，直到确认剩余条件的结果不会影响已经计算的结果。如果结果甚至在表达式的完整计算之前就很清楚，它就会短路，结果就会被返回。短路评估避免了不必要的工作，并导致高效的处理。

**AND( & &)短路:**在 AND 的情况下，表达式被求值，直到我们得到一个错误的结果，因为结果总是错误的，与进一步的条件无关。如果存在带有& &(逻辑与)的表达式，并且第一个操作数本身为假，则发生短路，不对进一步的表达式求值并返回假。

**示例:**使用 AND( & &)运算符短路。

```
<script>

// Since first operand is false and operator
// is AND, Evaluation stops and false is
// returned.
console.log(false && true && true && false)

// Whole expression will be evaluated.
console.log(true && true && true)
</script>
```

**输出:**

```
false
true

```

**OR(||)短路:**在 OR 的情况下，表达式被求值，直到我们得到一个真实的结果，因为结果将总是真实的，与进一步的条件无关。如果有一个表达式带有||(逻辑或)，并且第一个操作数本身为真，则发生短路，计算停止，并返回假。

**示例:**使用 OR(||)短路。

```
<script>

// First operand is true and operator is ||, 
// evaluation stops and true is returned.
console.log(true || false || false)

// Evaluation stops at the second operand(true).
console.log(false || true || true || false)
</script>
```

**输出:**

```
true
true

```