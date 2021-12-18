# JavaScript WeakSet

> 原文:[https://www.geeksforgeeks.org/javascript-weakset/](https://www.geeksforgeeks.org/javascript-weakset/)

下面是 **weakSet.add()** 方法的例子。

*   **例:**

    ```
    <script>  
        function gfg() {  
        var weakSetObject = new WeakSet();
        var objectOne = {};

        // add(value)
        weakSetObject.add(objectOne);
        document.write("objectOne added </br>");

        // has(value)
        document.write("WeakSet has objectTwo : " + 
                        weakSetObject.has(objectTwo));
        }  
        gfg();  
    </script>
    ```

*   **输出:**

    ```
    objectOne added
    ```

JavaScript 中的 WeakSet 用于存储对象的集合。它采用与集合相同的属性，即不存储副本。WeakSet 与 Set 的主要区别在于，WeakSet 是对象的集合，而不是某种特定类型的值。

**语法:**

```
new WeakSet(object)

```

**参数:**这里参数“对象”是可迭代对象。可迭代对象的所有元素都被添加到 WeakSet 中。

**一些不同的 WeakSet 函数:**

| 方法 | 描述 |
| --- | --- |
| 添加(值) | 一个新的对象被附加给 weakset 的给定值。
WeakSet_Object.add(值) |
| 删除(值) | 从 WeakSet 集合中删除该值。
WeakSet_Object.delete(值) |
| 具有(值) | 如果该值存在于 WeakSet 集合中，则返回 true，否则返回 false。
WeakSet_Object.has(值) |
| 长度() | 返回 weakSetObject 的长度
WeakSet_Object.length() |

**展示 WeakSet()函数工作原理的 JavaScript 代码:**

```
<script>

    var weakSetObject = new WeakSet();
    var objectOne = {};
    var objectTwo = {};

    // add(value)
    weakSetObject.add(objectOne);
    document.write("objectOne added <br>");
    weakSetObject.add(objectTwo);
    document.write("objectTwo added <br>");

    // has(value)
    document.write("WeakSet has objectTwo : " + 
                    weakSetObject.has(objectTwo));

    // delete(value)
    weakSetObject.delete(objectTwo);
    document.write("<br>objectTwo deleted<br>");
    document.write("WeakSet has objectTwo : " + 
                    weakSetObject.has(objectTwo));

</script>                    
```

**输出:**

```
objectOne added 
objectTwo added 
WeakSet has objectTwo : true
objectTwo deleted
WeakSet has objectTwo : false
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   苹果 Safari
*   歌剧