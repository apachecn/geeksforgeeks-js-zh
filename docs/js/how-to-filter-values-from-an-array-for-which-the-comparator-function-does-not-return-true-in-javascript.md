# 如何从 JavaScript 中比较器函数不返回真的数组中过滤值？

> 原文:[https://www . geesforgeks . org/如何从比较器函数不返回真值的数组中筛选值/](https://www.geeksforgeeks.org/how-to-filter-values-from-an-array-for-which-the-comparator-function-does-not-return-true-in-javascript/)

任务是根据传递给给定函数的返回值过滤数组。

目的是在数组中循环并执行一个将返回*真*或*假的函数。*然后过滤掉函数(比较器函数)不返回*真*的所有值。

**方法:**如果给定的数组是[5，6，7，8，9，2，6，3，-4，0，-9，-6]，并且任务是过滤掉负值并想要打印该值。

让我们创建一个函数，如果值为正，则返回*真*，否则返回*假*。

**JavaScript 代码:**

## 【JavaScript】

```
<script>
// Comparator function
const myFilter = (element) => {
  if(element >= 0){
      return true;
  }
  else{
      return false;
  }
} 
</script>
```

为了过滤掉数组，我们将遍历数组并调用这个函数“ *myFilter* ”。如果该值返回*真*，如果该函数返回*假*，则跳过该值，然后我们将使用“**过滤器将该值存储在*过滤器中。*** [**推()**](https://www.geeksforgeeks.org/javascript-array-push-method/) 【经过滤的数组。我们使用 [*forEach*](https://www.geeksforgeeks.org/javascript-array-foreach-method/) 循环遍历数组元素。

**例 1:**

## Javascript

```
<script>
    const arr = [5, 6, 7, 8, 9, 2, 6, 3, -4, 0, -9, -6];

    // Filtered array for which function
    // returned false
    var filteredArr = [];

    // Comparator function
    const myFilter = (element) => {
        if (element >= 0) {
            return true;
        }
        else {
            return false;
        }
    }

    // Iterate through each element 
    arr.forEach(element => {

        // Push in the filteredArr if 
        // it returns false
        if (myFilter(element) === false) {
            filteredArr.push(element);
        }
    })

    console.log("After filtering:", filteredArr);
</script>
```

**输出:**

```
After filtering : [ -4, -9, -6 ]
```

**示例 2:** 要过滤正值，我们可以更改我们的 **myFilter** 函数或 *forEach* 循环的代码部分。如果我们将 **myFilter** 函数中的条件更改为小于零，该函数将返回 *false* 作为正值。我们将这些正值存储在*过滤器或*中。

## JavaScript

```
<script>

    // Data to filter
    const arr = [5, 6, 7, 8, 9, 2, 6, 3, -4, 0, -9, -6];

    // Filtered array for which function
    // returned false
    var filteredArr = [];

    // Comparator function
    const myFilter = (element) => {
        if (element < 0) {
            return true;
        }
        else {
            return false;
        }
    }

    // Iterate through each element 
    arr.forEach(element => {

        // Push in the filteredArr if
        // function return false
        if (myFilter(element) === false) {
            filteredArr.push(element);
        }
    })

    console.log("After filtering :", filteredArr);
</script>
```

**输出:**

```
After filtering : [ 5, 6, 7, 8, 9, 2, 6, 3, 0 ]
```

我们已经成功过滤了函数不返回*真*的数组。