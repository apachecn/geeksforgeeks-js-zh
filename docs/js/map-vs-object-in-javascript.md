# JavaScript 中的地图 vs 对象

> 原文:[https://www.geeksforgeeks.org/map-vs-object-in-javascript/](https://www.geeksforgeeks.org/map-vs-object-in-javascript/)

是一种数据结构，有助于以成对的形式存储数据。该对由唯一的键和映射到该键的值组成。它有助于防止口是心非。
**[对象](https://www.geeksforgeeks.org/objects-in-javascript/)** 遵循与地图相同的概念，即使用键值对存储数据。但是有一些细微的差别，这使得 map 在某些情况下表现更好。

基本区别如下:

1.  在对象中，键字段的数据类型仅限于整数、字符串和符号。而在 Map 中，关键字字段可以是任何数据类型(整数、数组，甚至是对象！)
2.  在地图中，元素的原始顺序保持不变。就物体而言，情况并非如此。
3.  地图是一个对象的实例，反之亦然。

**示例:**

```
<script>
    var map = new Map([
        [5, 4],
        [7, 9]
    ]);

    //output:true
    console.log(map instanceof Object); 

    //output:false
    var obj = new Object();
    console.log(obj instanceof Map); 
</script>
```

**输出:**

```
true
false
```

让我们深入探讨一些使对象不同于地图的概念。

1.  **声明:**
    在 JavaScript 中，创建对象的方法有很多。例如:
    *   By using direct literal:

        ```
        var obj = {};
        var obj = {1:"Object Name", 2:"Test"};
        console.log(obj);
        ```

        **输出:**

        ```
        Object
        ```

    *   Use of constructor:

        ```
        var obj = new Object(); //Empty object
        var obj = new Object;
        console.log(obj);
        ```

        **输出:**

        ```
        Object
        ```

    *   Using object.create

        ```
        function fruits() {
                this.name = 'fruit 1';
                this.season = 'summer';
                }

                function apple() {
                fruits.call(this);
                }

                apple.prototype = Object.create(fruits.prototype);
                const app = new apple();
                console.log(app.name);
                console.log(app.season);
        ```

        ```
        fruit 1
        summer
        ```

        另一方面，地图只有一种创作方式。

    *   ```
        var map = new Map();//Empty
        console.log(map);
        var map = new Map([[1, "Sam"], [2, "John"]]); // 1-> Sam, 2->John
        console.log(map);
        ```

        **输出:**

        ```
        Map(0)
        Map(2)
        ```

2.  **访问元素:**
    *   地图使用其内置的 **get()方法**来访问其元素。

        ```
        map.get(1);
        ```

    *   对象只是使用带有点操作符的*‘键’*名称来访问其元素。

        ```
        obj.id;
        obj[id];
        ```

3.  **检查密钥是否已经存在:**
    *   地图使用它的内置 has()函数。

        ```
        map.has(1);//returns boolean value true or false.
        ```

    *   对象使用“===”运算符来执行任务。

        ```
        var doExist = obj.1 === undefined; //returns boolean value.
        ```

4.  **添加新元素:**
    *   Map 使用 set()方法添加新元素。

        ```
        map.set(4, 5); //{5->4, 7->9, 4->5}
        ```

    *   在 object 中，它是直接完成的。

        ```
        obj["Demo"]="Map vs Object"; //{1->Object Name, 2->Test, Demo->Map vs Object}
        ```

5.  **获取尺寸:**
    *   地图自动更新其大小，并获得最简单的。

        ```
        console.log(map.size);
        ```

    *   在对象中，需要使用 help object.keys()手动计算大小。

        ```
        console.log(object.keys(obj).length);
        ```

因此，我们可以看到 Map 有更好的性能和更少的代码编写结构，这使它比 Object 有优势。但是，有些场景需要使用对象。让我们看看。
**何时何地使用物体:**

*   对于我们需要简单的结构来存储数据，并且需要的键类型是整数、字符串或符号的情况，对象是一个很好的选择。
*   需要对单个属性元素应用单独逻辑的场景，对象绝对是首选。
*   JSON 直接支持对象，但不支持地图。
*   映射完全是散列的，而对象不止如此。

虽然地图往往比对象更有优势，但归根结底，这取决于所使用的数据类型和需要执行的操作。
然而，在 map 相对于 object 的所有优势中，map 无法取代 JavaScript 中的 object，因为 Object 远不止是一个哈希表。如果有其他选择，它不应该仅仅用于散列的目的。