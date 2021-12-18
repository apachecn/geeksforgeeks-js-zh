# 如何在 JavaScript 中编写一个返回大于数字的数组元素的函数？

> 原文:[https://www . geesforgeks . org/如何编写返回数组元素的函数-大于 javascript 中的数字/](https://www.geeksforgeeks.org/how-to-write-a-function-that-returns-array-elements-larger-than-a-number-in-javascript/)

给定一个数组 **arr** 和数字 **n** ，任务是编写一个函数，返回一个项目大于 n 的数组

**示例:**

```
Input:   arr = [65, 16, 0, 6, 64, 1, 68]
         n = 16
Output:  [65, 64, 68]

Input:   arr = [6, 46, 54, 6, 56, 54, 65, 4, 65]
        n =50
Output: [54, 56, 54, 65, 65]
```

为此，我们有以下方法:

#### 方法 1:使用数组过滤器()

在这种方法中，我们使用 **Array.filter** 方法。在每次迭代中，我们检查该值是否大于*数*。

**示例:**

## java 描述语言

```
<script>
let returnLarger = (arr, num) => arr.filter(n => n > num);

console.log(returnLarger( [65, 16, 0, 6, 64, 1, 68], 16))
console.log(returnLarger([6, 46, 54, 6, 56, 54, 65, 4, 65], 50))
</script>
```

**输出:**

```
[65, 64, 68]
[54, 56, 54, 65, 65]
```

#### 方法 2:使用 Array.reduce()

在这种方法中，我们使用 array.reduce 方法。使用空数组初始化累加器，并在每次迭代时检查当前值是否大于 *num* ，然后将当前值与累加器连接并返回，否则按原样返回累加器。

**示例:**

## java 描述语言

```
<script>
// Creating a function that return an array 
// whose items are less than num
let returnLarger = (arr, num) => {
  return arr.reduce((acc, curr)=>{  
    if(curr > num){
      return acc.concat(curr)  // Concatenate the acc with arr
    }else{
      return acc
    }
  }, [])   // Initialize the accumulator with an empty array
}

console.log(returnLarger( [65, 16, 0, 6, 64, 1, 68], 16))
console.log(returnLarger([6, 46, 54, 6, 56, 54, 65, 4, 65], 50))
</script>
```

**输出:**

```
[65, 64, 68]
[54, 56, 54, 65, 65]
```

#### 方法 3:使用数组映射方法:

在这种方法中，我们使用 map 方法迭代数组，并且在每次迭代时，我们检查当前值是否大于 *num* ？如果为真，那么我们就按原样返回值。如果为假，则用空字符串(或任何假值)替换该项。之后使用过滤方法去除虚假值。

## java 描述语言

```
<script>
// Creating a function that return an array 
// whose items are less than num
let returnLarger = (arr, num) => {
  return arr.map(v => v > num ? v : "").filter(Boolean)
}

console.log(returnLarger( [65, 16, 0, 6, 64, 1, 68], 16))
console.log(returnLarger([6, 46, 54, 6, 56, 54, 65, 4, 65], 50))
</script>
```

**输出:**

```
[65, 64, 68]
[54, 56, 54, 65, 65]
```

#### **方法 4:使用 for 循环:**

在这种方法中，我们创建一个空数组，并使用 for 循环迭代给定的数组，每次迭代时，我们检查当前值是否大于 *num* 。如果为真，那么我们将该值放入新创建的数组中。

## java 描述语言

```
<script>
// Creating a function that return an array 
// whose items are less than num

let returnLarger = (arr, num) => {
  let newArr = []

  for(let i = 0; i < arr.length; i++){
    if(arr[i] > num){
      newArr.push(arr[i])
    }
  }

  return newArr
}

console.log(returnLarger( [65, 16, 0, 6, 64, 1, 68], 16))
console.log(returnLarger([6, 46, 54, 6, 56, 54, 65, 4, 65], 50))
</script>
```

**输出:**

```
[65, 64, 68]
[54, 56, 54, 65, 65]
```