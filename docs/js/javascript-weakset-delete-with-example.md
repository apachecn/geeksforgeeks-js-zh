# JavaScript weakSet.delete()方法

> 原文:[https://www . geesforgeks . org/JavaScript-weakset-delete-with-example/](https://www.geeksforgeeks.org/javascript-weakset-delete-with-example/)

下面是 **weakSet.add()** 方法的例子。

*   **例:**

    ```
    <script>  
        function gfg() {  
    const A = new WeakSet(); 
    const B = {}; 
    A.delete(B); 

    document.write(A.has(B) +"<br>"); 
        }  
        gfg();  
    </script>
    ```

*   **输出:**

    ```
    false
    ```

**weakSet.delete()** 是 JavaScript 中的一个内置函数，用于从 [weakSet](https://www.geeksforgeeks.org/javascript-weakset/) 对象中删除特定元素。

**语法:**

```
weakSet.delete(A);
```

**参数:**它接受一个参数“A”，这是一个将要从 weakset 对象中删除的值。

**返回值:**如果元素已经成功从 weakset 对象中移除，则返回 true 如果元素没有成功移除或在 weakset 中找不到元素，则返回 false。

**显示该功能工作情况的 JavaScript 代码:**
**代码#1:**

```
<script>

   // Constructing weakSet() object
   const A = new WeakSet();

   // Creating a new element
   const B = {};

   // Adding the element to the weakset object
   A.add(B);

   // Testing whether the element has been
   // set into the weakset object or not
   document.write(A.has(B) +"<br>");

   // Deleting B form the weakSet() object
   A.delete(B);

   // Testing whether the element "B" has been deleted or not
   document.write(A.has(B) +"<br>");

</script>
```

**输出:**

```
true
false
```

这里的输出一开始为真，表示元素“B”已经成功设置到 weakSet 对象中，之后为假，表示元素“B”已经成功从 weakSet 对象中删除。

**支持的浏览器:**

*   谷歌 Chrome 36 及以上
*   Firefox 34 及以上版本
*   Apple Safari 9 及以上版本
*   歌剧 23 及以上
*   边缘 12 及以上