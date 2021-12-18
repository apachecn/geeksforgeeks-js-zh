# 在 JavaScript 中引用和复制变量

> 原文:[https://www . geeksforgeeks . org/引用并复制 javascript 中的变量/](https://www.geeksforgeeks.org/reference-and-copy-variables-in-javascript/)

在本文中，我们将讨论 JavaScript 中的按值传递和按引用传递。
JavaScript 总是通过值传递，但是在数组或对象中，值是对它的引用，所以你可以“改变”数据。JavaScript 有 5 种通过值传递的原始数据类型，它们是*布尔*、*空*、*未定义*、*字符串*和*数字*。它有 3 种通过引用传递的非原语数据类型，分别是*数组*、*函数*、*对象*。在非原始数据类型中，我们在复制数据方面面临一些挑战。正如我们所知，对象是在计算机内存的某个地方创建的。当我们声明任何属性时，它会在内存中创建一个空间。

**示例:**地址是一种数据类型，通过值传递，就像数字、字符串和地址指向内存中的位置一样。

**数字情况下按值传递。**

```
<script>
let age = 100;
let age2 = age;
document.write(age, age2);
document.write("<br>");
age = 200;
document.write(age, age2); 
</script>
```

**输出:**

```
100 100
200 100

```

**字符串情况下按值传递**

```
<script>
let name = 'sam';
let name2 = name;
document.write(name, name2); 
document.write("<br>");
name = 'xyz';
document.write(name, name2); 
</script>
```

**输出:**

```
sam sam
xyz sam

```

**数组情况下通过引用**

```
<script>
const players = ['Sam', 'Sarah', 'Ryan', 'Poppy'];
const team = players;
document.write(players, team);
</script>
```

**输出:**

```
["Sam", "Sarah", "Ryan", "Poppy"]
["Sam", "Sarah", "Ryan", "Poppy"]

```

现在，如果您更改“团队”数组中的数据，它也会影响“玩家”数组

```
<script>
const players = ['Sam', 'Sarah', 'Ryan', 'Poppy'];
const team = players;
team[3] = 'xyz';
document.write(players, team);
</script>
```

**输出:**

```
["Sam", "Sarah", "Ryan", "Poppy"]
["Sam", "Sarah", "Ryan", "xyz"]

```

这是数组引用，不是数组副本。它们都指向同一个数组。
我们有 4 种方法可以做到。通过使用这些方法，主阵列不会改变。

1.  **By using slice() method:**

    ```
    <script>
    const players = ['Sam', 'Sarah', 'Ryan', 'Poppy'];
    const playersCopy = players.slice();
    playersCopy[2]="west";
    console.log(players, palyersCopy);
    </script>
    ```

    **输出:**

    ```
    ["Sam", "Sarah", "Ryan", "Poppy"]
    ["Sam", "Sarah", "west", "Poppy"]

    ```

2.  **By using concat() method:** Create a new array variable and then concatenate the older one in the new array.

    ```
    <script>
      const players = ['Sam', 'Sarah', 'Ryan', 'Poppy'];
      const playersCopy2 = [].concat(players);
      playersCopy2[2]='hell';
      document.write(players, playersCopy2);
    </script>
    ```

    **输出:**

    ```
    ["Sam", "Sarah", "Ryan", "Poppy"]
    ["Sam", "Sarah", "hell", "Poppy"]

    ```

3.  **By using ES6 Spread operator:**

    ```
    <script>
     const players = ['Sam', 'Sarah', 'Ryan', 'Poppy'];
     const playersCopy3 = [...players];
     playersCopy3[3] = 'heeee hawww'; 
     document.write(players, playersCopy3);
    </script>
    ```

    **输出:**

    ```
      ["Sam", "Sarah", "Ryan", "Poppy"]
      ["Sam", "Sarah", "Ryan", "heeee hawww"]

    ```

4.  **By using Array.from():**

    ```
    <script>
      const players = ['Sam', 'Sarah', 'Ryan', 'Poppy'];
      const playersCopy4 = Array.from(players);
      playersCopy4[3]="kim";  
      document.write(players, playersCopy4);
    </script>
    ```

    **输出:**

    ```

    ["Sam", "Sarah", "Ryan", "Poppy"]
    ["Sam", "Sarah", "Ryan", "kim"]

    ```

**通过对象中的引用:**同样的点也适用于对象，它也会影响原始对象。

```
const person = {
      name: 'loren isum',
      age: 80
    };
const captain = person;
person.age = 25;
console.log(captain, person);
```

**输出:**

```
{name: "loren isum", age: 25}
{name: "loren isum", age: 25}

```

有两种方法可以做到。

1.  **By using the assign() method:**

    ```
    <script>
    const personObject = {
          name: 'loren isum',
          age: 80
        };
    const personCopy = Object.assign({}, 
        personObject, { number: 99, age: 12 });
    personCopy.age = 78;
    console.log(personCopy, personObject);
    </script>
    ```

    **输出:**

    ```
    {name: "loren isum", age: 78, number: 99}
    {name: "loren isum", age: 80}

    ```

2.  **By using the Spread operator:**

    ```
    <script>
    const personData = {
          name: 'loren isum',
          age: 80
        };
    const personCopy2 = {...personData };
    personCopy2.age = 78;
    console.log(personCopy2, personData );
    </script>
    ```

    **输出:**

    ```
    {name: "loren isum", age: 78}
    {name: "loren isum", age: 80}

    ```

还有一件事你需要考虑一下，在一个等式和等式运算符的情况下会发生什么。当我们在引用类型变量上使用这些运算符时，它们会检查引用。如果属性引用了同一个项目，那么比较将输出“真”，否则返回“假”

```
<script>
 var arrayReference = ["Hi!"];
 var arrayCopy = arrayReference;
 console.log(arrayCopy === arrayReference); 
</script>
```

**输出:**

```
 true

```

```
<script>
var array1 = ['Hi!'];
var array2 = ['Hi!'];
console.log(array1 === array2);
</script>
```

**输出:**

```
false

```

这可以通过字符串化数组来纠正。

```
<script>
var arr1str = JSON.stringify(array1);
var arr2str = JSON.stringify(array2);
console.log(arr1str === arr2str); // true
</script>
```

**输出:**

```
  true

```

我们可以更改对象人的名称属性，但由于引用人已被标记为*常量，因此无法重置引用人。*

```
<script>
 const person = {
   name: 'Tammy'
 };

// Name property changed
 person.name = 'abc'; 

// Objects are a reference type
 var val1 = { name: "Tom" };   
   var val2 = { name: "Tom" };
   console.log(val1 == val2)  
</script>
```

**输出:**

```
 false

```

但是我们可以通过字符串化数组来纠正这个问题。

```
<script>
 var array1 = ['Hi!'];
 var array2 = ['Hi!'];
 var arr1str = JSON.stringify(array1);
 var arr2str = JSON.stringify(array2);
 console.log(arr1str === arr2str); 
</script>
```

**输出:**

```
  true

```

**在函数的情况下通过引用传递:**如果我们在函数中传递对象，它会改变两个对象。

```
<script>
function changevalue(person) {
    var newPersonObj = (person);
    newPersonObj.age = 25;
    return newPersonObj;
}
var alex = {
    name: 'xyz',
    age: 30
};
var alexChanged = changevalue(alex);
console.log(alex); 
console.log(alexChanged); 
</script>
```

**输出:**

```
{ name: 'xyz', age: 25 }
{ name: 'xyz', age: 25 }

```

我们可以通过解析和字符串化对象来解决这个问题。

```
<script>
function changevalue(person) {
    var newPersonObj = JSON.parse(JSON.stringify(person));
    newPersonObj.age = 25;
    return newPersonObj;
}
var alex = {
    name: 'xyz',
    age: 30
};
var alexChanged = changevalue(alex);
console.log(alex); 
console.log(alexChanged);  
</script>
```

**输出:**

```
  { name: 'xyz', age: 30 }
  { name: 'xyz', age: 25 }

```