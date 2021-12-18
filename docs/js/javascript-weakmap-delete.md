# JavaScript weakMap.delete()方法

> 原文:[https://www.geeksforgeeks.org/javascript-weakmap-delete/](https://www.geeksforgeeks.org/javascript-weakmap-delete/)

下面是 **weakMap.delete()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
    function gfg() {
const weakmap = new WeakMap();

const key = {};
weakmap.set(key, 6);

document.write(weakmap.delete(key));
    }
    gfg();
</script>
```

*   **输出:**

```
true
```

**weakMap.delete()** 是 JavaScript 中的一个内置函数，用于从 weakMap 对象中删除特定元素。
**语法:**

```
weakMap.delete(key);
```

**参数:**它接受一个参数“key”，它是将要从对象 weakMap 中删除的元素的键。
**返回值:**如果该元素已从 weakMap 对象中删除，则返回 true 如果该键不在 weakMap 对象中，则返回 false。
**例:**

```
Input: weakmap1.delete(key1)
Output: true
```

**显示该功能工作情况的 JavaScript 代码:**
**代码#1:**

## java 描述语言

```
<script>

   // Creating a WeakMap() object
   const weakmap1 = new WeakMap();

   // Creating a key "key1"
   const key1 = {};

   // Setting the value 6 with key1 to the
   // the end of weakMap object
   weakmap1.set(key1, 6);

   // Deleting key of the element from
   // the weakMap object
   document.write(weakmap1.delete(key1));

</script>
```

**输出:**

```
true
```

这里的输出为真，这意味着元素的键已被成功删除。
**代码#2:**

## java 描述语言

```
<script>

   // Creating a WeakMap() object
   const weakmap1 = new WeakMap();

   // Creating a key "key1"
   const key1 = {};

   // Deleting key of the element from
   // the weakMap object
   document.write(weakmap1.delete(key1));

</script>
```

**输出:**

```
false
```

这里的输出是假的，因为带有任何值的键“key1”没有被设置到 weakMap 对象的末尾。

**支持的浏览器:**

*   Chrome 36 及以上
*   边缘 12 及以上
*   Firefox 6 及以上版本
*   Internet Explorer 11 及以上版本
*   歌剧 23 及以上
*   Safari 8 及以上