# 在 JavaScript 中 map . delete()

> 原文:[https://www.geeksforgeeks.org/map-delete-javascript/](https://www.geeksforgeeks.org/map-delete-javascript/)

**什么是 JavaScript 中的地图？**

*   Map 是 JavaScript 中的一种数据结构，允许存储[键、值]对，其中任何值都可以用作键或值。
*   地图集合中的键和值可以是任何类型，如果使用集合中已存在的键将值添加到地图集合中，则新值将替换旧值。
*   映射对象中元素的迭代是按照插入顺序进行的，并且“for…”循环为每次迭代返回一个所有[key，value]对的数组。

**JavaScript 中对象和地图的区别**
这两种数据结构在很多方面都是相似的，比如两者都使用键存储值，允许使用键检索那些值，删除键并验证键是否保存任何值。然而，在 JavaScript 中，对象和地图之间有很大的区别，这使得在许多情况下使用地图成为更好、更可取的选择。

*   地图中使用的键可以是任何类型的值，如函数、对象等，而对象中的键仅限于符号和字符串。
*   使用 size 属性可以很容易地知道地图的大小，但是在处理对象时，必须手动确定大小。
*   在需要频繁添加和移除[键、值]对的情况下，应该首选映射，因为映射是一种迭代数据类型，可以直接迭代，而迭代对象需要以特定方式获取其键。

**JavaScript 中的 Map.delete()方法**
JavaScript 中的 Map.delete()方法用于删除地图中存在的所有元素中的指定元素。

Map.delete()方法获取需要从映射中移除的键，从而移除与该键关联的元素并返回 true。如果密钥不存在，则返回 false。

**应用:**

*   Map.delete()用于删除映射中所有元素中与键相关联的元素。

**语法:**

```
my_map.delete(key)

```

> ***所用参数:***
> 
> *   *键:* *与此键相关的元素将从地图*中移除
> 
> **返回值:**
> 
> *   Map.delete()方法返回 true，如果存在要移除其关联元素的键，该键作为参数传递，否则返回 false。

示例:

```
Input :  my_map.set(1, 'first');
         my_map.set(2, 'second');
         my_map.set(3,'third');
         my_map.set(4,'fourth');

         document.write(my_map.delete(3));

Output : true

```

**解释:**键‘3’出现在地图中，因此与之相关的元素被移除并返回 true

```
Input :  my_map.set(1, 'first');
         my_map.set(2, 'second');
         my_map.set(3,'third');
         my_map.set(4,'fourth');

         document.write(my_map.delete(5));

Output : false

```

**解释:**键“5”不在地图中，因此返回假。

**代码 1:**

```
<script>
// creating a map object
var my_map = new Map();

// Adding [key, value] pair to the map
my_map.set(1, 'first');
my_map.set(2, 'second');
my_map.set(3,'third');
my_map.set(4,'fourth');

// will display true as key '3'
// is present and its associated  
// element is removed as well
document.write(my_map.delete(3),"</br>","</br>");

// elements left in the map after deletion
document.write("key-value pair of the map",
                " after deletion-","</br>");

my_map.forEach(function (item, key, mapObj) 
{ 
    document.write(key.toString(),":",
                   " ",item.toString() + "<br />"); 
}); 

</script>                        
```

输出:

```
true

key-value pair of the map after deletion-
1: first
2: second
4: fourth

```

**代码 2:**

```
<script>
// creating a map object
var my_map = new Map();

// Adding [key, value] pair to the map
my_map.set(1, 'first');
my_map.set(2, 'second');
my_map.set(3,'third');
my_map.set(4,'fourth');

// will display false as key '5'
// is not present and its associated  
// element is removed as well
document.write(my_map.delete(5),
               "</br>","</br>");

// elements left in the map after deletion
document.write("key-value pair of the map",
               " after deletion-","</br>");

my_map.forEach(function (item, key, mapObj) { 
    document.write(key.toString(),":"," ",
                   item.toString() + "<br />"); 
}); 

</script>                    
```

输出:

```
false

key-value pair of the map after deletion-
1: first
2: second
3: third
4: fourth

```

**Error and Exception:**

*   If the key passed as an argument to the function is not present in the map then it returns false. Basically, it neither throws any exception nor does it have any error.

    **map . clear()的工作差异 Map.erase()和此功能**
    Map.clear()会移除地图的所有键值对，并将地图的大小减小到零。而 Map.erase()移除指定的映射值，该值的键作为参数或迭代器在范围内传递以移除对。

    支持的浏览器:

    *   Chrome 38 及以上
    *   边缘 12 及以上
    *   Firefox 13 及以上版本
    *   Internet Explorer 11 及以上版本
    *   歌剧 25 及以上
    *   safari 8 及以上