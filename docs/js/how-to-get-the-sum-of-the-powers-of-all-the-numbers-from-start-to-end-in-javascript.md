# 如何在 JavaScript 中得到所有数字从头到尾的幂的和？

> 原文:[https://www . geesforgeks . org/如何用 javascript 从头到尾计算所有数字的幂的和/](https://www.geeksforgeeks.org/how-to-get-the-sum-of-the-powers-of-all-the-numbers-from-start-to-end-in-javascript/)

给定三个变量*开始、结束*和*功率*。我们的任务是找出从*开始*到*结束*之间的所有数字的总和。

**示例 1:** 起始变量 1 结束 5 和功率 2。从 1 到 5 迭代，并将每一个都提升到 2 的幂。将所有元素 1+4+9+16+25 相加，即 55。

```
Input: 1, 5, 2
Output: 55
```

**例 2:**

```
Input: 1, 5, 3
Output: 225
```

**方法 1:** 我们可以通过以下方法得到想要的答案。在这种方法中，我们使用 [*为*](https://www.geeksforgeeks.org/javascript-for-loop/) 循环来解决我们的问题。简单的方法是使用*进行*循环，从开始到结束进行迭代，并遵循以下步骤。

*   使变量 *ans* 存储我们的 *ans。*
*   将各元件升至*功率*的功率。
*   将每个凸起的元素添加到*和*变量中。
*   返回〔t0〕年〔t1〕年。

**示例:**

## java 描述语言

```
<script>
    // Function that that return sum of
    // All elmetn raised to power
    function PowerNo( s, num, power)
    {
      var ans = 0;
      for( let i = s; i <= num; i++)
      {
        let temp = i**power;

        ans += temp;
      }
      return  ans;
    }
    // Test variable
    var a1 = PowerNo(1, 5, 2);
    var a2 = PowerNo(1, 5, 3);
    var a3 = PowerNo(5, 5, 4);
    // Printing result
    console.log(a1)
    console.log(a2)
    console.log(a3)
</script>
```

**输出:**

```
55
225
625
```

**方法 2:** 在这个方法中，我们使用 [*映射()*](https://www.geeksforgeeks.org/map-in-javascript/) 和 [*reduce()*](https://www.geeksforgeeks.org/javascript-array-reduce-method/) 的方法来解决我们的问题。 *map()* 函数用于迭代数组并对所有元素执行函数，并返回一个具有修改值的新数组。 *reduce()* 方法用于用所有元素执行一个函数，将其存储在一个变量中并返回。

*   我们有*开始、*T2【结束、和*力量*变量。
*   制作从*开始*范围到*结束*范围值的范围数组。
*   在数组中使用*映射()*方法，将所有数字加到*幂*的幂。
*   在更新后的数组中使用 *reduce()* 方法，对所有元素求和。
*   最后， *reduce()* 返回总和。

**示例:**

## java 描述语言

```
<script>
  // function that perform raiesing  number to power
  function PowerNo(num, i, power) {
    return (num + i) ** power;
  }
  // function that perform sum to all the element
  function SumNo(x, y) {
    return x + y;
  }
  // function performing map() and reduce( ) ot array
  const sumPower = (num, s, power) =>
    Array(num + 1 - s)
      .fill(0)
      .map((x, i) => PowerNo(s, i, power))
      .reduce((x, y) => SumNo(x, y), 0);

  // test case
  var a1 = sumPower(5, 1, 2);
  var a2 = sumPower(5, 1, 3);
  var a3 = sumPower(5, 5, 4);

  // printing answer
  console.log(a1);
  console.log(a2);
  console.log(a3);
</script>
```

**输出:**

```
55
225
625
```