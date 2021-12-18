# 如何在 JavaScript 中检查变量是否不为空？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中检查变量是否不为空/](https://www.geeksforgeeks.org/how-to-check-if-a-variable-is-not-null-in-javascript/)

通过对给定变量应用简单的 [**if-else**](https://www.geeksforgeeks.org/if-else-statement-in-javascript/) 条件，您可以很容易地在 JavaScript 中检查变量是 **Null** 还是 **Not Null** 。

有两种方法可以检查变量是否为空。首先，我将讨论一开始对您来说似乎正确的错误方法，然后我们将讨论检查变量是否为空的正确方法。

**方法 1:** 看似正确的错误方式。

**条件:**

```
if(my_var) {
    ....
}
```

**注意:**当变量为空时，变量中不存在任何对象值。**空**经常在一个可以期待一个对象，但没有对象相关的地方被检索到。

根据上述条件，如果 *my_var* 为空，那么给定的 ***如果*** 条件将不会执行，因为空在 JavaScript 中是一个 *falsy* 值，但是在 JavaScript 中有许多预定义的 falsy 值，比如

*   **未定义**
*   **零**
*   **0**
*   **(空字符串)**
*   ****假****
*   ****NaN****

**因此，如果 *my_var* 等于任何上述预定义的虚假值，那么 ***如果*** 条件将不会执行，反之亦然。**

****例 1:****

## **超文本标记语言**

```
<!DOCTYPE html>
<html> 
<body style="text-align:center;">

    <h2 style="color:green;">
        GeeksforGeeks
    </h2>

<p>
        variable-name : GFG_Var
    </p>

    <button onclick="myGeeks()">
        Check for vowel
    </button>

    <h3 id="div" style="color:green;">HTML</h3>

    <!-- Script to check existence of variable -->
    <script>
        function myGeeks() {

            var h3 = document.getElementById("div");

            var GFG_Var = h3.innerHTML;

          // check if GFG_Var variable contain any vowels
          // HTML text contains no vowels,
          // so variable my_var will be assigned null 
           const my_var = GFG_Var.match(/[aeiou]/gi);  

            if (my_var ) {
                h3.innerHTML = "Variable is not null";
            }
            else {
                h3.innerHTML = "Variable is NULL";
            }
        }
    </script>
</body>
</html>                    
```

****输出:****

**![](img/ac60109e14cd618e750522cdf9284510.png)

检查元音** 

****方法 2:** 下面的代码展示了检查变量是否为空的正确方法。**

****条件:****

```
**if(my_var !== null)**
**{**
    **....**
**}**
```

**上述条件实际上是检查变量是否为空的正确方法。如果 *my_var* 不是空值，即**

*   **如果 my_var 为*未定义* ，则条件将执行。**
*   **如果 my_var 为 *0* ，则条件将执行。**
*   **如果 my_var 为**“**(空字符串)，则条件执行。**
*   **…**

**这个条件将检查变量的确切值是否为空。**

****例 2:****

## **超文本标记语言**

```
<!DOCTYPE html>
<html>
<body style="text-align:center;">

    <h2 style="color:green;" >
        GeeksforGeeks
    </h2>

<p>
        variable-name : GFG_Var
    </p>

    <button onclick="myGeeks()">
        Check for vowel
    </button>

    <h3 id="div" style="color:green;">HTML</h3>

    <!-- Script to check existence of variable -->
    <script>
        function myGeeks() {

            var h3 = document.getElementById("div");

            var GFG_Var = h3.innerHTML;

          // check if GFG_Var variable contain any vowels
          // HTML text contain no vowels
          // so variable my_var will assign null 
           const my_var = GFG_Var.match(/[aeiou]/gi);  

            // this will check exactly whether variable is null or not
            if (my_var !== null ) {
                h3.innerHTML = "Variable is not null";
            }
            else {
                h3.innerHTML = "Variable is NULL";
            }
        }
    </script>
</body>

</html>                    
```

****输出:**输出与第一个示例相同，但 JavaScript 代码中有适当的条件。**

**![](img/4b2be09092955bd1936f00b26732c127.png)**