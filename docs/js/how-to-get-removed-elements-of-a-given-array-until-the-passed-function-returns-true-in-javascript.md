# 在 JavaScript 中，如何获取给定数组的移除元素，直到传递的函数返回 true？

> 原文:[https://www . geesforgeks . org/如何移除给定数组的元素，直到传递的函数在 javascript 中返回 true/](https://www.geeksforgeeks.org/how-to-get-removed-elements-of-a-given-array-until-the-passed-function-returns-true-in-javascript/)

**JavaScript** 中的数组有很多方法，使得很多操作变得容易。

在本文中，让我们看看如何在传递的函数返回一些东西之前获取移除的元素的不同方法。

让我们取一个排序的数组，任务是移除所有小于传递给函数的限制器值的元素，我们需要打印所有移除的元素。

**方法 1:** 使用 [**切片()**](https://www.geeksforgeeks.org/javascript-string-slice/) 方法

在一个函数中，如果有多个返回语句，那么只有第一个返回语句被执行，函数被完成。

**代码片段:**

```
var retrieveRemoved = function (arg_1, arg_2) {
    var i;
    for (i = 0; i < array.length; i++) {
        if (condition) {
            return statement1;
        }
    }

    return statement2;
}
```

**例:**

## java 描述语言

```
<script> 

 var array = [1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8];

 // Removing elements less than 5 and returning them 

 var limiter = 5;

 // function which slices the array taking limiter as parameter
 var retrieveRemoved = function (array, limiter) {
     var i;
     for (i = 0; i < array.length; i++) {
     // If the number value is greater or equal than limiter
         if (array[i] >= limiter) {

             // It takes the array from 0th 
             // index to i, excluding it
             return array.slice(0, i);
         }
     }

     return array.slice(i);
 }
 var removed = retrieveRemoved(array, limiter);
 console.log("The removed elements: " + removed);
</script>
```

**Output:**

```
The removed elements: 1,2,2,3,4
```

**方法 2:** 使用另一个数组。另一个数组可以用来检查条件。如果它不满足条件，这些是要删除的元素。我们将所有不满足条件的元素推入另一个数组，并返回结果数组。

**例:**

## java 描述语言

```
<script>  
  var array = [1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8];

  // Removing elements less than 5 and returning them
  var limiter = 5;

  var retrieveRemoved = function (array, limiter) {
      var i,s;
      var res=[];
      for (i = 0; i < array.length; i++) {
          if (array[i] < limiter) {

              // Push() method is used to 
              // values into the res[].        
              res.push(array[i]);    
          }
          else{
              s=i;
              break;
          }
      }
      return res;

      return array.slice(i);
  }
  var removed = retrieveRemoved(array, limiter);
  console.log("The removed elements are: " + removed);
</script>
```

**Output:**

```
The removed elements are: 1,2,2,3,4
```