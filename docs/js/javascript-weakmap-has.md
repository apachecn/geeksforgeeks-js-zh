# JavaScript weakMap.has()方法

> 原文:[https://www.geeksforgeeks.org/javascript-weakmap-has/](https://www.geeksforgeeks.org/javascript-weakmap-has/)

下面是 **weakMap.has()** 方法的例子。

*   **例:**

    ```
    <script> 
        function gfg() { 
    const weakmap = new WeakMap(); 
    const key = {}; 
    weakmap.set(key, 'gfg'); 

    document.write(weakmap.has(key)); 
        } 
        gfg(); 
    </script> 
    ```

*   **输出:**

    ```
    true
    ```

**weakMap.has()** 是 JavaScript 中的一个内置函数，用于返回一个布尔值，该值指示 weakMap 对象中是否存在具有特定键的元素。

**语法:**

```
weakMap.has(key);
```

**参数:**它接受一个参数“键”，该参数是将被测试是否存在于目标武器中的元素的键。

**返回值:**如果 weakmap 对象中存在具有指定键的元素，则返回真，否则返回假。

**示例:**

```
Input: weakmap1.has(key1)
Output: true

```

**JavaScript 来展示这个功能的工作方式:**
**代码#1:**

```
<script>

   // Creating a WeakMap() object
   const weakmap1 = new WeakMap();

   // Creating a key "key1"
   const key1 = {};

   // setting element 'gfg' to the key "key1"
   weakmap1.set(key1, 'gfg');

   // Testing whether the key is present 
   // in the weakMap() object or not
   document.write(weakmap1.has(key1));

</script>
```

**输出:**

```
true
```

**代码#2:**

```
<script>

   // Creating a WeakMap() object
   const weakmap1 = new WeakMap();

   // Creating a key "key1"
   const key1 = {};

   // Testing whether the key is present 
   // in the weakMap() object or not
   document.write(weakmap1.has(key1));

</script>
```

**输出:**

```
false
```

这里的输出是假的，因为键“key1”没有被设置在 weakMap 对象的末尾。

**支持的浏览器:**

*   谷歌 Chrome 36 及以上
*   边缘 12 及以上
*   Firefox 6 及以上版本
*   Internet Explorer 11 及以上版本
*   歌剧 23 及以上
*   Safari 8 及以上