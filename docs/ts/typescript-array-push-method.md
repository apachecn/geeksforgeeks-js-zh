# 排版|数组推送()方法

> 原文:[https://www.geeksforgeeks.org/typescript-array-push-method/](https://www.geeksforgeeks.org/typescript-array-push-method/)

**Array.push()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于在数组的最后一个元素中添加给定的元素，并返回新数组的长度。
**语法:**

```
 array.push(element1, ..., elementN)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **element1、…、elementN :** 此参数是要添加到数组末尾的元素。

**返回值:**这个方法返回新数组的长度。
以下示例说明了打字稿中的**数组推送()**方法:

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of push() method 
    var val = arr.push(8)

    // printing element
    console.log( arr );
</script>
```

**输出:**

```
[11,89,23,7,98,8]

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [2, 5, 6, 3, 8, 9]; 
    var val,j=0;

    // use of push() method    
    for(j=0; j<4 ; j++){
      var y = arr[j];
      var x = y * j;
      val = arr.push(x);
    }
    // printing element
    console.log( arr );
</script>
```

**输出:**

```
[2,5,6,3,8,9,0,5,12,9]

```