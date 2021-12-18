# JavaScript 数组键()方法

> 原文:[https://www.geeksforgeeks.org/javascript-array-keys-method/](https://www.geeksforgeeks.org/javascript-array-keys-method/)

下面是**数组键()**方法的例子。

*   **例:**

    ```
    <script>

       // Taking input as an array A 
       // containing some elements.
       var A = [ 5, 6, 10 ];

       // array.keys() method is called
       var iterator = A.keys();

       // printing index array using the iterator
       for (let key of iterator) {
        document.write(key + ' ');
       }
    </script>
    ```

*   **输出:**

    ```
    0 1 2
    ```

**array.keys()** 方法用于返回一个新的数组迭代器，该迭代器包含给定输入数组中每个索引的键。

**语法:**

```
array.keys()
```

**参数:**此方法不接受任何参数。

**返回值:**返回一个新的数组迭代器。

下面的例子说明了 JavaScript 中的**数组键()**方法:

*   **Example:**

    ```
    var A = [ 'gfg', 'geeks', 'cse', 'geekpro' ];
    var iterator = A.keys(document.write(key + ' '));
    ```

    **输出:**

    ```
    0 1 2 3
    ```

上述方法的代码如下:
**程序 1:**

```
<script>

   // Taking input as an array A 
   // containing some elements.
   var A = [ 'gfg', 'geeks', 'cse', 'geekpro' ];

   // array.keys() method is called
   var iterator = A.keys();

   // printing index array using the iterator
   for (let key of iterator) {
    document.write(key + ' ');
   }
</script>
```

**输出:**

```
0 1 2 3 
```

**程序 2:**

```
<script>

  // Taking input as an array A
  // containing some elements
  var A = [ 'gfg', 'geeks', 'cse', 'geekpro', '', 1, 2 ];

  // array.keys() method is called
  var iterator = A.keys();

  // Printing index array using the iterator
  for (let key of iterator) {
    document.write(key + ' ');
  }
</script>
```

**输出:**

```
0 1 2 3 4 5 6 
```

**支持的浏览器:**JavaScript**数组键()**方法支持的浏览器如下:

*   谷歌 Chrome 38.0
*   微软边缘 12.0
*   Mozilla Firefox 28.0
*   Safari 8.0
*   Opera 25.0