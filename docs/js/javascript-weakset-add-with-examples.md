# JavaScript weakSet.add()方法

> 原文:[https://www . geesforgeks . org/JavaScript-weakset-add-with-examples/](https://www.geeksforgeeks.org/javascript-weakset-add-with-examples/)

下面是 **weakSet.add()** 方法的例子。

*   **例:**

    ```
    <script>  
        function gfg() {  
        const weakset = new WeakSet(); 

        const object1 = {}; 
        weakset.add(object1); 
        document.write(weakset.has(object1));  
        }  
        gfg();  
    </script>
    ```

*   **输出:**

    ```
    true
    ```

**weakSet.add()** 是 JavaScript 中的一个内置函数，用于在对象 [WeakSet](https://www.geeksforgeeks.org/javascript-weakset/) 的末尾添加一个对象。WeakSet 对象允许您在集合中存储弱持有的对象。

**语法:**

```
weakSet.add(A);
```

**参数:**它接受参数“A”，这是一个要添加到 weakset 对象的值。

**返回值:**返回 weakset 对象。

**示例:**

```
Input: weakset.add(object1); 
Output: true

```

<center>**JavaScript code to show the working of the this function:**</center>

**Code #1:**

```
<script>

    // Constructing a weakset object
    const weakset = new WeakSet();

    // Constructing a new object object1
    const object1 = {};
    const object2 = {};
    const object3 = {};
    const object4 = {};

    // Adding the object1 at the end of the weakset object.
    weakset.add(object1);
    weakset.add(object2);
    weakset.add(object3);
    weakset.add(object4);

    // Printing either object has been added or not
    document.write(weakset.has(object1) +"<br>");
    document.write(weakset.has(object2) +"<br>");
    document.write(weakset.has(object3) +"<br>");
    document.write(weakset.has(object4));

</script>
```

**输出:**

```
true
true
true
true
```

**代码#2:**

```
<script>

    // Constructing a weakset object
    const weakset = new WeakSet();

    // Constructing a new object object1
    const object1 = {};
    const object2 = {};
    const object3 = {};
    const object4 = {};

    // Printing either object has been added or not
    document.write(weakset.has(object1) +"<br>");
    document.write(weakset.has(object2) +"<br>");
    document.write(weakset.has(object3) +"<br>");
    document.write(weakset.has(object4));

</script>
```

**输出:**

```
false
false
false
false
```

这里的输出是假的，因为新创建的对象还没有设置到 weakSet()对象的末尾。

**支持的浏览器:**

*   谷歌 Chrome 36 及以上
*   Firefox 34 及以上版本
*   Apple Safari 9 及以上版本
*   歌剧 23 及以上
*   边缘 12 及以上