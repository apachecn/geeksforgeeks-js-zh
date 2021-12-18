# 如何在 JavaScript 中将 2D 数组转换为逗号分隔值(CSV)字符串？

> 原文:[https://www . geesforgeks . org/how-convert-a-2d-array-to-a-逗号分隔值-csv-string-in-javascript/](https://www.geeksforgeeks.org/how-to-convert-a-2d-array-to-a-comma-separated-values-csv-string-in-javascript/)

给定一个 2D 数组，我们必须使用 JS 将其转换为逗号分隔值(CSV)字符串。

```
Input:
[ [ "a" , "b"] , [ "c" ,"d" ] ]
Output:
"a,b 
 c,d"
Input:
[ [ "1", "2"]
["3", "4"]
["5", "6"] ]
Output:
"1,2
3,4
5,6"
```

为此，我们必须了解一些在这方面有帮助的阵列原型函数:

**Join 函数:**array . prototype . Join()函数用于用一个字符/字符串连接数组中的所有字符串。

**示例:**

```
[ "a","b"].join( ",") will result in : "a,b"
```

**Map 函数:**array . prototype . Map()返回一个新数组，该数组包含调用我们提供的函数对每个元素的结果。

**示例:**

```
arr= ["a","b"]

// Adding "c" to each element
newArray = arr.map( item => item + "c") 
value of newArray = ["ac", "bc"]
```

**方法:**我们将使用 map 函数和 join 函数将每个 1D 行组合成一个字符串，中间用逗号分隔。然后使用 join 函数用“\n”连接所有单个字符串。

**示例:**

## java 描述语言

```
<script>
// Create CSV file data in an array  
var array2D = [ 
                [ "a" , "2"] ,
                [ "c" ,"d" ] 
              ];

// Use map function to traverse on each row
var csv = array2D
  .map((item) => {

    // Here item refers to a row in that 2D array
    var row = item;

    // Now join the elements of row with "," using join function
    return row.join(",");
  }) // At this point we have an array of strings
  .join("\n");

  // Join the array of strings with "\n"
console.log(csv);
</script>
```

**输出:**

```
a,2
c,d
```

**解释:**我们首先使用 2D 数组上的 map 函数遍历每一行，然后使用 join 函数使用逗号连接该行中的元素数组。接下来，该映射函数返回一个字符串数组，我们使用“\n”将它连接起来。从而产生一个 CSV 字符串。

**替代方法:**我们甚至可以使用 for 循环来遍历数组，而不是地图。

**示例:**

## java 描述语言

```
<script>
var csv="";
create CSV file data in an array  
var array2D = [ 
                [ "a" , "2"] ,
                [ "c" ,"d" ] 
              ];

for (var index1 in array2D) {
  var row = array2D[index1];

  // Row is the row of array at index "index1"
  var string = "";

  // Empty string which will be added later
  for (var index in row) {
    // Traversing each element in the row
    var w = row[index];

    // Adding the element at index "index" to the string
    string += w;
    if (index != row.length - 1) {
      string += ",";
      // If the element is not the last element , then add a comma
    }
  }
  string += "\n";

  // Adding next line at the end
  csv += string;
  // adding the string to the final string "csv"
}
console.log(csv);
</script>
```

```
Output:
a,2
c,d
```