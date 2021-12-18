# JavaScript |索引集合

> 原文:[https://www . geesforgeks . org/JavaScript-indexed-collections/](https://www.geeksforgeeks.org/javascript-indexed-collections/)

**索引集合**是具有数字索引的集合，即按索引值排序的数据集合。

在 JavaScript 中，数组是一个索引集合。数组是具有数值索引的有序值集。例如，一个名为“学生”的数组包含学生的姓名，索引值是学生的人数。JavaScript 没有显式数组数据类型。但是，我们可以在 JavaScript 中使用预定义的 Array 对象及其方法来处理数组。

**创建数组:**创建和初始化数组的方法有很多，如下所示:

*   创建数组而不定义数组长度。在这种情况下，长度等于参数的数量。

    ```
    var arr = new Array( element0, element1, ... );   
    var arr = Array( element0, element1, ... );       
    var arr = [ element0, element1, ... ];  
    ```

*   创建一个给定大小的数组

    ```
    var arr = new Array(6); 

    var arr = Array(6);

    var arr = [];
    arr.length = 6;
    ```

*   创建一个可变长度数组，并根据需要添加许多元素。

    ```
    // First method: Initialize an empty
    // array then add elements
    var students = [];
    students [0] = 'Sujata Singh';
    students [1] = 'Mahesh Kumar';
    students [2] = 'Leela Nair';

    // Second method: Add elements to
    // an array when you create it
    var fruits = ['apple', ‘mango', 'Banana'];
    ```

**访问数组元素:**使用索引访问数组元素。数组的索引从零开始，这意味着元素的索引从零开始。

```
<script>

var fruits = ['Apple', 'Mango', 'Banana']; 
console.log(fruits [0]); 
console.log(fruits[1]);  

</script>
```

**输出:**

```
Apple
Mango
```

**获取数组长度:**要获取数组的长度，请使用 array_name.length 属性。

```
<script>

var fruits = ['Apple', 'Mango', 'Banana']; 

console.log(fruits.length)

</script>
```

**输出:**

```
3
```

**迭代数组:**迭代数组元素的方法有很多。

*   **使用 for 循环:** for 循环提供了编写循环结构的简洁方式。与 while 循环不同，for 语句在一行中消耗初始化、条件和递增/递减，从而提供一个更短、更易于调试的循环结构。

    ```
    <script>

    var fruits = ['Apple', 'Mango', 'Banana']; 
    for (var i = 0; i < fruits.length; i++) {
      console.log(fruits[i]);
    }

    </script>
    ```

    **输出:**

    ```
    Apple
    Mango
    Banana
    ```

*   **使用 [forEach()循环](https://www.geeksforgeeks.org/javascript-array-foreach/):**forEach()函数为数组的每个元素提供一次。所提供的函数可以对给定数组的元素执行任何类型的操作。

    ```
    <script>

    var fruits = ['Apple', 'Mango', 'Banana'];  
    fruits.forEach( function(fruit) {
        console.log(fruit);
    });

    </script>
    ```

    ```
    Apple
    Mango
    Banana
    ```

*   **使用带箭头功能的 forEach Loop:**

    ```
    <script>

    var fruits = ['Apple', 'Mango', 'Banana'];  

    fruits.forEach(fruit => console.log(fruit)); 

    </script>
    ```

    ```
    Apple
    Mango
    Banana
    ```

**数组方法:**我们可以使用各种数组方法来处理数组。这些是:

*   **[push() Method](https://www.geeksforgeeks.org/javascript-array-prototype-push-function/):** This method adds one or more elements to the end of an array and returns the resulting length of the array.

    ```
    <script>

    var numbers = new Array('1', '2');

    numbers.push('3');

    console.log(numbers);

    </script>
    ```

    **输出:**

    ```
    ["1","2","3"]
    ```

*   **[pop()方法](https://www.geeksforgeeks.org/javascript-array-prototype-pop/) :** 此方法从数组中移除最后一个元素并返回该元素。

    ```
    <script>

    var numbers = new Array('1', '2', '3');

    var last = numbers.pop(); 

    console.log(last);

    </script>
    ```

    ```
    3
    ```

*   **[concat() Method](https://www.geeksforgeeks.org/javascript-array-prototype-concat-function/):** This method join two arrays and returns a new array.

    ```
    <script>

    var myArray = new Array('1', '2', '3');

    myArray = myArray.concat('a', 'b', 'c'); 

    console.log(myArray);

    </script>
    ```

    **输出:**

    ```
    ["1","2","3","a","b","c"]
    ```

*   **[join() Method](https://www.geeksforgeeks.org/javascript-array-join-method/):** This method creates a string by joining all the elements of an array.

    ```
    <script>

    var students = new Array('john', 'jane', 'joe');

    var list = students.join(' - ');

    console.log(list);

    </script>
    ```

    **输出:**

    ```
    john - jane - joe
    ```

*   **[sort() Method](https://www.geeksforgeeks.org/javascript-array-sort/):** This method sorts the elements of an array.

    ```
    <script>

    var myArray = new Array('West', 'East', 'South');

    myArray.sort(); 

    console.log(myArray);

    </script>
    ```

    **输出:**

    ```
    ["East","South","West"]
    ```

*   **[indexOf() Method](https://www.geeksforgeeks.org/javascript-array-indexof/):** This method searches the array for Element and returns the index of the first occurence of element.

    ```
    <script>

    var myArr = ['a', 'b', 'a', 'b', 'a'];

    console.log(myArr.indexOf('b'));

    </script>
    ```

    **输出:**

    ```
    1
    ```

*   **[shift() Method](https://www.geeksforgeeks.org/javascript-array-prototype-shift/):** This method removes the first element from an array and returns that element.

    ```
    <script>

    var myArr = new Array('a', 'b', 'c');

    var first = myArr.shift(); 

    console.log(first);

    </script>
    ```

    **输出:**

    ```
    a
    ```

*   **[reverse() Method](https://www.geeksforgeeks.org/javascript-array-prototype-reverse/):** This method reverse the first array element becomes the last and the last becomes the first. It transposes all the elements in an array in this manner and returns a reference to the array.

    ```
    <script>

    var myArr = new Array('a', 'b', 'c');

    myArr.reverse(); 

    console.log(myArr);

    </script>
    ```

    **输出:**

    ```
    ["c","b","a"]
    ```

*   **[map() Method](https://www.geeksforgeeks.org/javascript-array-map-method/):** This method returns a new array of the returned value from executing function on every array item.

    ```
    <script>

    var myArr1 = ['a', 'b', 'c'];

    var a2 = myArr1.map(function(item) { 
        return item.toUpperCase(); 
    });

    console.log(a2);

    </script>
    ```

    **输出:**

    ```
    ["A","B","C"]
    ```

*   **[filter() Method](https://www.geeksforgeeks.org/javascript-array-filter/):** This method returns a new array containing the items for which function returned true.

    ```
    <script>

    var myArr1 = ['a', 10, 'b', 20, 'c', 30];

    var a2 = myArr1.filter(function(item) { 
        return typeof item === 'number'; 
    });

    console.log(a2);

    </script>
    ```

    **输出:**

    ```
    [10,20,30]
    ```