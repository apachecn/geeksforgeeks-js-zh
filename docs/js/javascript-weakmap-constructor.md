# JavaScript WeakMap()构造函数

> 原文:[https://www . geesforgeks . org/JavaScript-weak map-constructor/](https://www.geeksforgeeks.org/javascript-weakmap-constructor/)

**WeakMap()构造函数**生成的 WeakMap 对象是一个键/值对数组，其中键被弱引用。键应该是对象，值可以是任意的。“地图”和“武器地图”的区别在于，关键点必须是对象，并且只能被弱引用。这意味着，如果没有其他对该键的强引用，垃圾收集器可以移除 WeakMap 中的元素。

**语法:**

```
new WeakMap( iterable )
```

**参数:**它接受一个可选参数，该参数可以是任何可迭代对象。iterable 是一个类似数组的对象，元素中有键值对。创建的 WeakMap 将包括每个键值对。null 被认为是未定义的。

以下示例说明了 WeakmMap 构造函数:

**示例:****get()**方法用于检索与键相关联的值。如果没有值与键相关联，它将返回 undefined。

## java 描述语言

```
<script>
  const o1 = {}, o2 = {};

  const wp = new WeakMap([[o2, 17]]);
  console.log(wp.get(o2));
  console.log(wp.get(o1));
</script>
```

**输出:**

```
17
undefined
```

**示例:**使用 **set()** 方法为键赋值。它返回 WeakMap 对象，该对象允许您链. set()调用。

## java 描述语言

```
<script>
  const o1 = {}, o2 = {};
  const wp = new WeakMap();

  wp.set(o1, 100).set(o2, 200);

  console.log(wp.get(o1));
  console.log(wp.get(o2));
</script>
```

**输出:**

```
100
200
```

**示例:****has()**方法用于确定具有给定键的元素是否存在于武器地图中。如果退出，则返回 true，否则返回 false。

## java 描述语言

```
<script>
  const o1 = {}, o2 = {};

  const wp = new WeakMap([[o2, 17]]);

  console.log(wp.has(o2));
  console.log(wp.has(o1));
</script>
```

**输出:**

```
true
false
```

**示例:****delete()**方法用于删除具有特定键的元素。如果元素存在并被移除，则返回 true 否则，返回 false。

## java 描述语言

```
<script>
  const o1 = {}, o2 = {};

  const wp = new WeakMap([[o1, 77]]);

  console.log(wp.delete(o2));
  console.log(wp.delete(o1));
</script>
```

**输出:**

```
false
true
```