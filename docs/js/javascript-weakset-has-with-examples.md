# JavaScript weakSet.has()方法

> 原文:[https://www . geesforgeks . org/JavaScript-weakset-has-with-examples/](https://www.geeksforgeeks.org/javascript-weakset-has-with-examples/)

下面是 **weakSet.add()** 方法的例子。

*   **例:**

    ```
    <script>  
        function gfg() {  
        const A = new WeakSet(); 
       const object = {}; 
       A.add(object); 
       document.write(A.has(object)); 
        }  
        gfg();  
    </script>
    ```

*   **输出:**

    ```
    true
    ```

**weakSet.has()** 是 JavaScript 中的一个内置函数，用于返回一个布尔值，该值指示对象是否存在于 [weakSet](https://www.geeksforgeeks.org/javascript-weakset/) 中。WeakSet 对象允许您在集合中存储弱持有的对象。

**语法:**

```
weakSet.has(A);
```

**参数:**它接受参数“A”，这是一个将要检查它是否存在于弱集对象中的值。

**返回值:**如果元素存在，则返回布尔值 true，否则返回 false。

**示例:**

```
Input: weakset.has(object1); 
Output: true

```

**显示该功能工作情况的 JavaScript 代码:**
**代码#1:**

```
<script>

   // Constructing a weakSet() object
   const A = new WeakSet();

   // Constructing new objects
   const object1 = {};

   // Adding the new object to the weakSet
   A.add(object1);

   // Checking whether the new object is present
   // in the weakSet or not
   document.write(A.has(object1) +"<br>");

</script>
```

**输出:**

```
true
```

这里输出为真，因为对象“object1”存在于 WeakSet()对象中。
**代码#2:**

```
<script>

   // Constructing a weakSet() object
   const A = new WeakSet();

   // Constructing new objects
   const object1 = {};

   // Checking whether the new object is present
   // in the weakSet or not
   document.write(A.has(object1) +"<br>");

</script>
```

**输出:**

```
false
```

这里输出为假，因为对象“object1”不在 WeakSet()对象中。

**支持的浏览器:**

*   谷歌 Chrome 36 及以上
*   Firefox 34 及以上版本
*   Apple Safari 9 及以上版本
*   歌剧 23 及以上
*   边缘 12 及以上