# 如何去除 JavaScript 数组中的重复元素？

> 原文:[https://www . geesforgeks . org/如何从 javascript 数组中移除重复元素/](https://www.geeksforgeeks.org/how-to-remove-duplicate-elements-from-javascript-array/)

有多种方法可以删除数组中的重复项。我们将讨论最常见的四种方式。

**使用** [**filter()方法**](https://www.geeksforgeeks.org/javascript-array-filter-method/)**:**filter()方法创建一个新的元素数组，通过我们提供的条件。它将只包括那些返回 true 的元素。我们可以通过简单地调整条件来从数组中删除重复的值。

## java 描述语言

```
<script>
    var arr = ["apple", "mango", "apple", 
            "orange", "mango", "mango"];

    function removeDuplicates(arr) {
        return arr.filter((item, 
            index) => arr.indexOf(item) === index);
    }

    console.log(removeDuplicates(arr));
</script>
```

**输出:**

```
["apple", "mango", "orange"]
```

**使用** [**Set()**](https://www.geeksforgeeks.org/sets-in-javascript/) **方法:**该方法使用 ES6 (ES2015)设置新的对象类型，允许您创建唯一值的集合。

## java 描述语言

```
<script>
    var arr = ["apple", "mango", "apple",
            "orange", "mango", "mango"];

    function removeDuplicates(arr) {
        return [...new Set(arr)];
    }

    console.log(removeDuplicates(arr));
</script>
```

**输出:**

```
["apple", "mango", "orange"]
```

**使用** [**forEach()方法**](https://www.geeksforgeeks.org/javascript-array-foreach-method/) **:** 通过使用 forEach()方法，我们可以迭代数组中的元素，如果数组中不存在新的元素，我们将推入新的数组。

## java 描述语言

```
<script>
    var arr = ["apple", "mango", 
        "apple", "orange", "mango", "mango"];

    function removeDuplicates(arr) {
        var unique = [];
        arr.forEach(element => {
            if (!unique.includes(element)) {
                unique.push(element);
            }
        });
        return unique;
    }

    console.log(removeDuplicates(arr));
</script>
```

**输出:**

```
["apple", "mango", "orange"]
```

**使用** [**reduce()方法**](https://www.geeksforgeeks.org/javascript-array-reduce-method/)**:**reduce()方法用于根据您传递的某个 reducer 函数，对数组的元素进行约简，并将其组合成最终的数组。

## java 描述语言

```
<script>
    var arr = ["apple", "mango", 
        "apple", "orange", "mango", "mango"];

    function removeDuplicates(arr) {
        var unique = arr.reduce(function (acc, curr) {
            if (!acc.includes(curr))
                acc.push(curr);
            return acc;
        }, []);
        return unique;
    }

    console.log(removeDuplicates(arr));
</script>
```

**输出:**

```
["apple", "mango", "orange"]
```