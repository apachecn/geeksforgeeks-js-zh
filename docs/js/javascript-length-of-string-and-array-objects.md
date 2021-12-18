# JavaScript 字符串长度属性

> 原文:[https://www . geesforgeks . org/JavaScript-字符串和数组长度-对象/](https://www.geeksforgeeks.org/javascript-length-of-string-and-array-objects/)

下面是字符串长度属性的示例。

*   **例:**

    ```
    <script> 
    // JavaScript to illustrate length property 

    function func() { 

        // length property for string 
        document.write("GFG".length) 
    } 
    func(); 
    </script> 
    ```

*   输出:

    ```
    3

    ```

JavaScript 对象的 length 属性用于找出该对象的大小。该属性用于许多对象，如 JavaScript 字符串、JavaScript 数组等。对于字符串，此属性返回字符串中的字符数。在数组的情况下，此属性返回数组中存在的元素数。

**语法:**

```
object.length
where the object can either be a string object or an array object

```

**示例:**

```
Input : print("GeeksForGeeks".length)
Output :13

Input : print([1, 2, 3, 4, 5, 6, 7, 8, 9].length)
Output :9

```

**解释:**
在第一个例子中，13 是字符串“GeeksForGeeks”中的字符数，因此输出是 13。
同样在第二个例子中，数组的长度是 9，输出也是 9

**程序:**

```
<script>
// JavaScript to illustrate length property

function func() {

    // length property for array
    document.write([1,2,3,4,5,6,7,8,9].length);
    document.write("<br>");

    // length property for string
    document.write("GeeksForGeeks".length)
}
func();
</script>
```

输出:

```
9
13

```