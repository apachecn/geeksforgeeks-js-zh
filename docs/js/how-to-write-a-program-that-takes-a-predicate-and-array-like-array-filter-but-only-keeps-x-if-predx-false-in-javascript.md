# 如何编写一个像 Array.filter()一样带谓词和数组，但在 JavaScript 中只有 pred(x)= = false 时才保留 x 的程序？

> 原文:[https://www . geesforgeks . org/如何编写一个带谓词和数组的程序数组过滤器但只能保留-x-if-predx-false-in-JavaScript/](https://www.geeksforgeeks.org/how-to-write-a-program-that-takes-a-predicate-and-array-like-array-filter-but-only-keeps-x-if-predx-false-in-javascript/)

JavaScript 中的**谓词**与 [**谓词**数学](https://www.geeksforgeeks.org/mathematic-logic-predicates-quantifiers/)相同，后者返回*真*或*假*。

谓词就像一个确定传递的参数是否满足给定条件的函数。谓词只返回*真*或*假*。

在本文中，让我们看看谓词在 JavaScript 中与函数一起传递时如何使用[](https://www.geeksforgeeks.org/array-data-structure/)**数组。**

****语法:****

```
function predicate(argument) 
{
     if(condition_satisfied)
     return true;
     else
     return false;
}
function using_predicate(array, predicate)
{
      for(elements in array )
      {
          if (predicate is satisfied)
          {
            code for satisfied condition;
          }
          else
          {
            code for else condition;
          }
      }
}
```

****示例 1:** 以下函数接受一个数组和谓词，并返回满足*pred(x)= = false 的结果数组*。在这个函数中，谓词返回*真，*如果数组元素是偶数，则返回*假*。输出应该是奇数。**

## **java 描述语言**

```
<script>
  function pred(x) {
      if (x % 2 == 0)
          return true;
      else
          return false;
  }

  function implementPredicate(array, pred) {
      var res = [];
      for (let i = 0; i < array.length; i++) {
          if (pred(array[i]) === false) {
              res.push(array[i]);
          }
      }
      return res;
  }
  var array = [1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8];
  var final = implementPredicate(array, pred);
  console.log("The resultant array is "+final);
</script>
```

****输出:****

```
The resultant array is 1,3,5,7
```

****使用带有 filter()方法的谓词:****

****语法:****

```
function predicate(argument) 
{
     if(condition_satisfied)
     return true;
     else
     return false;
}
array.filter(predicate);
```

****例 2:****

## **java 描述语言**

```
<script>
  function pred(x) {
      if (x % 2 == 0)
          return false;
      else
          return true;
  }

  var array = [1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8];
  var final = array.filter(pred);
  console.log("The resultant array is "+final);
</script>
```

****输出:****

```
The resultant array is 1,3,5,7
```

****示例 3:** 以下函数通过将参数作为数组和谓词传递给函数，使用谓词计算数组中 8 的频率。**

## **java 描述语言**

```
<script>
  function pred(x) {
      if (x == 8)
          return true;
      else
          return false;
  }
  function implementPredicate(array, pred) {
      var res = 0;
      for (let i = 0; i < array.length; i++) {
          if (pred(array[i]) === true) {
              res++;
          }
      }
      return res;
  }

  var array = [1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8];
  var final = implementPredicate(array, pred)
  console.log("The frequency of 8 is " + final);
</script>
```

****输出:****

```
The frequency of 8 is 3
```