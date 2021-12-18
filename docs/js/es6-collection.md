# 是 6 |集合

> 原文:[https://www.geeksforgeeks.org/es6-collection/](https://www.geeksforgeeks.org/es6-collection/)

ES6 是 JavaScript 中添加的一系列新功能。在 ES6 版本中，包含了新的数据类型集合，因此不再需要使用对象，并且以简单的方式实现事情变得更加容易。
在 ES6 版本中，JavaScript 引入了两个新东西。

*   地图
*   设置

**地图:**地图是任何类型的键和值的集合，简单来说**地图**是**键-值对**的集合。它像 JavaScript 中的一个对象一样工作。它返回一个新的或空的地图。
**语法:**

```
var map = new Map();
```

<figure class="table">

| **Method** | **Description** |
| 地图。大小() | It determines the number of key points or numerical values in the map. |
| 地图。设置() | It sets the value of the key. It requires two parameters, the key and the value of the key. |
| 地图。has() | It checks whether there is a key in the map and then returns *true* . |
| 地图。get() | It takes a value associated with a key. If the value is not available, it is undefined. |
| 地图。按键() | It returns an iterator for all keys in the map. |
| 地图。条目() | It returns a new iterator array containing the key-value pairs of each element in the insertion order. |
| 地图。值() | It returns an iterator for each value in the map. |
| 地图。删除() | Used to delete an entry. |
| 地图。清除() | It clears all key-value pairs from the map. |
| 地图。foreach() | It performs a **callback** function. This function is executed for each element in the map. |

</figure>

**代表…的循环:**代表**..的**是一个循环，它给出了一个非常简洁的语法来迭代所有种类的**可枚举数**和**可枚举数**。对可迭代对象的迭代。这个循环迭代数组、字符串、类似数组的对象、类型、映射和任何用户定义的可迭代对象。

*   **例:**

## java 描述语言

```
// Simple JavaScript program to illustrate for...of loop
<script>
var arr = ['a', 3 , 'b', 2 , 'c', 1 ,'d'];
document.write("array elements are : ");
for (let ele of arr) {
  document.write(ele+' ');
}
</script>
```

*   **输出:**

```
array elements are : a 3 b 2 c 1 d
```

**地图示例:**

*   **程序 1:** 实现 map.size()，map.set()方法

## java 描述语言

```
// Simple JavaScript program to implement Map.size
<script>
var m = new Map()
m.set('a', 1);
m.set('b', 2);
m.set('c', 3);
document.write(m.size);
</script>                   
```

*   **输出:**

```
size of the map is : 3
```

*   **程序二:**实现 map.set()，map.get()，map.delete()，map.clear()，map.has()方法

## java 描述语言

```
<script>
/ Simple JavaScript program with Map
var map = new Map();
map.set("website ", "Geeksforgeeks");
document.write("Website is - " +map.get("website "));
// Use "get()" function

map.set("Subject1", "JavaScript"); //use "set()" function
map.set("Subject2", "C++");
map.set("Subject3", "python");
document.write("<br>Is it contains JavaScript ? - "+map.has("Subject1"));
document.write("<br>Is it contains C++ ? - "+map.has("Subject2"));
document.write("<br>Is it contains python ? - "+map.has("Subject3"));
// Use "has()" function

map.delete("subject2");
document.write("<br>Delete C++");
// Use "delete()" function
document.write("<br>Is is contains C++ now ? - "+map.has("C++")); //false

map.clear();//use "clear()" function
document.write("<br>Delete whole map");
document.write("<br> Is it has any value now? - "+map.has("Subject1"));

</script>
```

*   **输出:**

```
Website is - Geeksforgeeks
Is it contains JavaScript ? - true
Is it contains C++ ? - true
Is it contains python ? - true
Delete C++
Is is contains C++ now ? - false
Delete whole map
Is it has any value now? - false
```

*   **程序 3:** 实现 map.forEach()方法

## java 描述语言

```
<script>
// Simple JavaScript program to implement <b>Map.forEach()</b>

var m = new Map()
m.set('a', 1);
m.set('b', 2);
m.set('c', 3);
m.forEach((k, v)=>document.write(`key: ${k} value: ${v} <br>`));
</script>
```

*   **输出:**

```
key: 1 value: a
key: 2 value: b
key: 3 value: c
```

*   **程序 4:** 实现 map.keys()方法

## java 描述语言

```
<script>
// Simple JavaScript program to implement Map.keys()

var m = new Map()
m.set('a', 1);
m.set('b', 2);
m.set('c', 3);
var i = m.keys();
document.write("value : "+ i.next().value+"<br>");//"a"
document.write("value : "+ i.next().value+"<br>");//"b"
document.write("value : "+ i.next().value+"<br>");//"c"
document.write("value : "+ i.next().value+"<br>");//undefined
// Because the map contains only 4 elements
</script>
```

*   **输出:**

```
value : a
value : b
value : c
value : undefined
```

*   **程序:5** 实施地图条目()方法

## java 描述语言

```
<script>
// Simple JavaScript program to implement Map.entries()

var m = new Map()
m.set('a', 1);
m.set('b', 2);
m.set('c', 3);
var i = m.entries();
document.write("value : "+ i.next().value+"<br>");//"a,1"
document.write("value : "+ i.next().value+"<br>");//"b,2"
document.write("value : "+ i.next().value+"<br>");//"c,3"
document.write("value : "+ i.next().value+"<br>");//undefined
// Because the map contains only 4 elements
</script>   
```

*   **输出:**

```
value : a,1
value : b,2
value : c,3
value : undefined
```

*   **程序 6:** 实现 map.values()方法。

## java 描述语言

```
<script>
// Simple JavaScript program to implement Map.values()

var m = new Map()
m.set('a', 1);
m.set('b', 2);
m.set('c', 3);
var i = m.values();
document.write("value : "+ i.next().value+"<br>");//"1"
document.write("value : "+ i.next().value+"<br>");//"2"
document.write("value : "+ i.next().value+"<br>");//"3"
document.write("value : "+ i.next().value+"<br>");//undefined
// Because the map contains only 4 elements
</script>   
```

*   **输出:**

```
value : 1
value : 2
value : 3
value : undefined
```

**弱图:**弱图与正常图相似。弱映射用于将弱对象引用存储为关键字，即关键字必须是对象。弱映射不能被清除，键值可以是垃圾值。

*   **例:**

## java 描述语言

```
<script>

// Simple JavaScript program to implement WeakMap()
var gfg = new WeakMap();
var gg = {};

//"gg" is a object
// Works as key
gfg.set(gg,"c++");
document.write(gfg.has(gg));//true
document.write("<br>"+gfg.get(gg));//c++
gg=null;//"gg" becomes null
document.write("<br>"+gfg.get(gg));//undefined
</script>
```

*   **输出:**

```
true
c++
undefined
```

**集合:**是 **ES6** 版本引入的数据结构。一个**集合**是一个像数组一样的值的集合，但是它不包含任何重复。它是**可变的**，所以我们的程序可以随时添加和删除值。返回**设定对象**。

<figure class="table">

| way | describe |
| 准备好。大小() | It returns the total number of values that exist in the collection. |
| 准备好。添加() | If there is no value in the collection, it will add the value to the collection. |
| 准备好。清除() | It removes all values from the collection. |
| 准备好。删除㈤ | It removes a value from the collection, which is passed as a parameter. |
| 准备好。has(v) | If the passed value "v" is in set, this method returns **true** . |
| 准备好。条目() | It returns an iterator object that contains an array that contains the entries of this collection. |
| set.values()和 set.keys() | They all return all values from set, similar to *map.values ()* . |
| set.forEach()方法 | Like **map.foreach ()** , it executes a callback function. This function is executed for each element in the collection. |

</figure>

*   **语法:**

```
var s = new Set("val1","val2","val3")
```

*   **例:**

## java 描述语言

```
<script>
// Simple JavaScript program with Set

var st = new Set();

st.add("JavaScript").add("C++").add("python"); //use "add()" function

document.write("<br>Is it contains JavaScript ? - "+st.has("JavaScript"));
document.write("<br>Is it contains C++ ? - "+st.has("C++"));
document.write("<br>Is it contains python ? - "+st.has("python"));
// Use "has()" function

st.delete("C++");
document.write("<br>Delete C++");

// Use "delete()" function
document.write("<br>Is is contains C++ now ? - "+st.has("C++")); //false

st.clear();//use "clear()" function
document.write("<br>Delete whole set");
document.write("<br> Is it has any value now? - "+st.has("JavaScript"));

</script>                   
```

*   **输出:**

```
Is it contains JavaScript ? - true
Is it contains C++ ? - true
Is it contains python ? - true
Delete C++
Is is contains C++ now ? - false
Delete whole set
Is it has any value now? - false
```

**迭代器:**集合中的迭代器允许一次访问一个对象集合。它与 next()方法一起工作，当调用 next()时，一次打印一个集合的值，并且在成功读取集合的值后，返回属于 **done** 属性的布尔值**“真”**。这件事是在控制台窗口发生的。在输出的情况下，如果我们使用关键字**“value”**后跟 next()，就像**迭代器一样，只会显示值。值**

*   **例:**

## java 描述语言

```
<script>
// Simple JavaScript program with Set iterator
var  s = new Set(['a','b','c']); //set elements
var itr = s.values();
document.write(itr.next().value+"<br>");
document.write(itr.next().value+"<br>");
document.write(itr.next().value+"<br>");
document.write(itr.next().value);//undefined
</script>   
```

*   **输出:**

```
a
b
c
undefined
```

**弱集:**类似于弱地图，也用于存储对象的集合。它类似于正常集，因此不能存储副本。它可能包含垃圾值。集合和弱集合的唯一区别是弱集合包含对象。

*   **例:**

## java 描述语言

```
<script>
var gfg = new WeakSet
var gg1 = {};//"gg1" is a object
var gg2 = {};//"gg2" is a object

gfg.add(gg1);
gfg.add(gg2);
document.write(gfg.has(gg1));//true
gfg.delete(gg1);//delete "gg1"
document.write("<br>"+gfg.has(gg1));//undefined
</script>   
```

*   **输出:**

```
true
false
```