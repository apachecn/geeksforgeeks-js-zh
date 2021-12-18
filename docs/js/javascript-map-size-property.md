# JavaScript Map.size 属性

> 原文:[https://www.geeksforgeeks.org/javascript-map-size-property/](https://www.geeksforgeeks.org/javascript-map-size-property/)

[映射](https://www.geeksforgeeks.org/map-in-javascript/)是元素的集合，其中每个元素都存储为键、值对。 **Map.size** 属性用于返回存储在地图中的键值对的数量。

**语法:**

```
mapName.size
```

**返回值:**表示存储在映射中的键、值对的数量的整数。

以下示例说明了 **Map.size** 属性:

**例 1:**

## java 描述语言

```
<script>

    // Creating a new map
    let GFGmap = new Map();

    // Adding key, value pairs to the map
    GFGmap.set('1', 'Apple');
    GFGmapset('2', 'Banana');
    GFGmap.set('3', 'Mango');

    // Printing number of key, value
    // pairs stored in the map
    console.log(GFGmap.size);

</script>
```

**输出:**

```
3
```

**例 2:**

## java 描述语言

```
<script>

    // Creating a new map
    let GFGmap = new Map();

    // Adding key, value pairs to the map
    GFGmap.set('a', 'Apple');
    GFGmapset('b', 'Ball');
    GFGmap.set('c', 'Cat');
    GFGmap.set('d', 'Dog');

    // Printing number of key, value
    // pairs stored in the map
    console.log(GFGmap.size);
</script>
```

**输出:**

```
4
```