# 如何在 JavaScript 中去除数组中的重复元素？

> 原文:[https://www . geesforgeks . org/如何从 javascript 数组中移除重复元素/](https://www.geeksforgeeks.org/how-to-remove-duplicate-elements-from-array-in-javascript/)

有各种不同的方法来查找数组中的副本。我们将讨论在数组中查找重复项的两种方法。

[**使用 Set:**](https://www.geeksforgeeks.org/sets-in-javascript/)Set 对象允许您存储任何类型的唯一值，无论是基元值还是对象引用。这是移除重复元素并从数组中获取唯一元素的最简单方法。

**示例:**假设我们有一个名为 *City* 的数组，它由重复的城市名称组成，我们希望移除重复的名称并从中找到唯一的元素。

## java 描述语言

```
<script>
  // Defining a set of the cities
  let city = [
    "surat",
    "ahmedabad",
    "rajkot",
    "mumbai",
    "surat",
    "delhi",
    "ahmedabad",
    "anand",
  ];

  // For removing the duplicate values
  // we are using the Set() function
  let unique_city = [new Set(city)];

  // Printing the unique cities
  console.log(unique_city);
</script>
```

**输出:**

```
["surat", "ahmedabad", "rajkot", "mumbai", "delhi"]
```

<strpng>使用 [**forEach()方法:**](https://www.geeksforgeeks.org/javascript-array-foreach-method/) 我们使用 JavaScript[**include()**](https://www.geeksforgeeks.org/javascript-array-includes-method/)函数，如果一个元素在数组中，该函数返回 *true* ，如果它不存在，则返回 *false* 。</strpng>

以下示例迭代数组的元素，并将元素添加到尚不存在的新数组中。

**例:**

## Javascript

```
<script>
  // Defining a set of the cities
  let city = [
    "surat",
    "ahmedabad",
    "rajkot",
    "mumbai",
    "surat",
    "delhi",
    "ahmedabad",
    "anand",
  ];

  // Defining the unique cities from the above
  // array by using forEach loop
  let unique_city = [];
  city.forEach((c) => {
    if (!unique_city.includes(c)) {
      unique_city.push(c);
    }
  });

  // Printing the unique cities
  console.log(unique_city);
</script>
```

**输出:**

```
["surat", "ahmedabad", "rajkot", "mumbai", "delhi"]
```