# JavaScript 数组从()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-from-method-2/](https://www.geeksforgeeks.org/javascript-array-from-method-2/)

下面是来自()方法的**数组的例子。**

*   **例:**

    ```
    <script>
        document.write(Array.from("This is JavaScript Array "+
                                  "from() Method"));
    </script>                                        
    ```

*   **输出:**

    ```
    T,h,i,s, ,i,s, ,J,a,v,a,S,c,r,i,p,t, ,A,r,r,a,y, 
     ,f,r,o,m,(,), ,M,e,t,h,o,d
    ```

**arr.from()** 方法用于根据给定的数组创建新的数组实例。在字符串的情况下，字符串的每个字母都被转换为新数组实例的一个元素，在整数值的情况下，新数组实例只接受给定数组的元素。

**语法:**

```
Array.from(object, mapFunction, thisValue)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**此参数保存将转换为数组的对象
*   **mapFunction:** 这个参数是可选的，用于调用数组的每一项。
*   **该值:**该参数是可选的，它保存要传递的上下文，以便在执行映射函数时使用。如果传递了上下文，它将像这样用于回调函数的每次调用，否则使用 undefined 作为默认值。

**返回值:**返回一个新的数组实例，其元素与给定数组相同。在字符串的情况下，字符串的每个字母都被转换为新数组实例的一个元素。

下面的例子说明了 JavaScript 中的**数组 from()** 方法:

*   **示例 1:** 在这里，我们看到输出创建了一个新数组，其内容与整数情况下的输入相同。

    ```
    Input : 10, 20, 30
    Output:  Array [10, 20, 30]

    ```

*   **示例 2:** 在这里，我们看到输出创建了一个新数组，其内容与输入相同字符串的每个字母都转换为新数组实例的一个元素。

    ```
    Input : geeksforgeeks
    Output: Array ["g", "e", "e", "k", "s", "f", "o", 
                   "r", "g", "e", "e", "k", "s"]

    ```

上述方法的代码如下:
**程序 1:**

```
<script>
    document.write(Array.from("GeeksforGeeks"));
    document.write("<br />")
    document.write(Array.from([10, 20, 30]));
</script>                    
```

**输出:**

```
G,e,e,k,s,f,o,r,G,e,e,k,s
10,20,30

```

**程序 2:**

```
<script>
    // Here input array is [1,2,3] and output 
    // become bouble of each elements.
    document.write(Array.from([1, 2, 3], 
                                x => x + x));
</script>                                        
```

**输出:**

```
2,4,6
```

**注意:**如果我们取一个复数作为参数，它会返回一个错误，因为只有数组和字符串可以作为参数。

**支持的浏览器:**JavaScript**Array from()**方法支持的浏览器如下:

*   谷歌 Chrome 45.0
*   微软边缘 12.0
*   Mozilla Firefox 32.0
*   Safari 9.0
*   Opera 25.0