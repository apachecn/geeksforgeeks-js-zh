# JavaScript weakMap.get()方法

> 原文:[https://www.geeksforgeeks.org/javascript-weakmap-get/](https://www.geeksforgeeks.org/javascript-weakmap-get/)

下面是 **weakMap.get()()** 方法的例子。

*   **例:**

    ```
    <script> 
        function gfg() { 

    const weakmap1 = new WeakMap(); 

    const key1 = {}; 

    weakmap1.set(key1, 12); 

    document.write(weakmap1.get(key1)); 
        } 
        gfg(); 
    </script> 
    ```

*   **输出:**

    ```
    12
    ```

**weakMap.get()** 是 JavaScript 中的一个内置函数，用于从 weakMap 对象中返回特定元素。

**语法:**

```
weakMap.get(key);
```

**参数:**它接受一个参数“键”，该参数是将从对象 weakmap 返回的元素的键。

**返回值:**返回与 WeakMap 对象中特定键相关联的元素，如果找不到键，则返回未定义。

**示例:**

```
Input: weakmap1.get(key1)
Output: 42

```

**JavaScript 代码展示 weakmap()的工作原理功能:**
T3】代码#1:

```
<script>

   // Creating a WeakMap() object
   const weakmap1 = new WeakMap();

   // Creating a key "key1"
   const key1 = {};

   // setting value 42 with key "key1" in the 
   // object weakMap
   weakmap1.set(key1, 42);

   // Getting the specified elements i.e, 42
   document.write(weakmap1.get(key1));

</script>
```

**输出:**

```
42
```

**代码#2:**

```
<script>

   // Creating a WeakMap() object
   const weakmap1 = new WeakMap();

   // Creating a key "key1"
   const key1 = {};

   // Getting the specified elements
   document.write(weakmap1.get(key1));

</script>
```

**输出:**

```
undefined
```

这里的输出是未定义的，因为键“key1”没有在 weakMap 对象的末尾设置。

**支持的浏览器:**

*   谷歌 Chrome 36 及以上
*   边缘 12 及以上
*   Firefox 6 及以上版本
*   Internet Explorer 11 及以上版本
*   歌剧 23 及以上
*   Safari 8 及以上