# JavaScript Map()构造函数

> 原文:[https://www.geeksforgeeks.org/javascript-map-constructor/](https://www.geeksforgeeks.org/javascript-map-constructor/)

地图()[构造器](https://www.geeksforgeeks.org/javascript-object-constructors/)用于在 JavaScript 中创建[地图](https://www.geeksforgeeks.org/map-in-javascript/)对象。映射是一种数据结构，将元素存储为键和值对。

**语法:**

```
new Map()
new Map(iterable)
```

**参数:**

*   **可迭代的:**一个[可迭代的](https://www.geeksforgeeks.org/javascript-iterator/)对象，用于迭代元素，存储为一个键值对。

**返回值:**在地图构造器初始化后，一个新的地图对象返回。

**例 1:**

## java 描述语言

```
<script>

// map1 contains 
// 1 => 10
// 2 => 20
// 3 => 30
// 4 => 40
var map1 = new Map([
    [1 , 10], [2 , 20] ,
    [3, 30],[4, 40]
]);

console.log("Map1: ");
console.log(map1);
</script>
```

**输出:**

```
Map1: 
Map(4) { 1 => 10, 2 => 20, 3 => 30, 4 => 40 }
```

**例 2:**

## java 描述语言

```
<script>

// map2 contains 
// firstname => Ram
// lastname => Prasad
// website => geeksforgeeks 
var map2 = new Map([
    ["firstname" ,"Ram"], 
    ["lastname", "Prasad"], 
    ["website", "geeksforgeeks"]
]);

console.log("Map2: ");
console.log(map2);
</script>
```

**输出:**

```
Map2:
Map(3) {
 'firstname' => 'Ram',
 'lastname' => 'Prasad',
 'website' => 'geeksforgeeks'
}
```

**例 3:**

## java 描述语言

```
<script>

// Map contains nested array
var map3 = new Map([
    ["whole numbers", [1 ,2 ,3 ,4]],
    ["Decimal numbers" , [1.1, 1.2, 1.3, 1.4]],
    ["negative numbers", [-1, -2, -3, -4]]
]);

console.log("Map3: ");
console.log(map3);
</script>
```

**输出:**

```
Map3:
Map(3) {
 'whole numbers' => [ 1, 2, 3, 4],
 'Decimal numbers' => [ 1.1, 1.2, 1.3, 1.4],
 'negative numbers' => [ -1, -2, -3, -4]
}
```