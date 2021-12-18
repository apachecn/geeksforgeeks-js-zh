# 在 JavaScript 中不使用 map 方法如何映射数组值？

> 原文:[https://www . geesforgeks . org/如何在不使用 javascript 中的映射方法的情况下映射数组值/](https://www.geeksforgeeks.org/how-to-map-array-values-without-using-map-method-in-javascript/)

数组元素可以使用 JavaScript 中的[循环方法进行映射。](https://www.geeksforgeeks.org/loops-in-javascript/) [map()](https://www.geeksforgeeks.org/javascript-array-map-method/) 方法用数组中每个元素调用的函数的输出结果创建一个新数组。这也可以用 JavaScript 中的 [for 循环](https://www.geeksforgeeks.org/javascript-for-loop/)来实现。

**方法:**对此，我们可以创建两个数组，其中一个数组包含要映射的数组元素，第二个数组存储对应函数的所有返回值。我们可以使用 [JavaScript Array push()](https://www.geeksforgeeks.org/javascript-array-push-method/) 方法在输出数组中推送函数的返回值。

**语法:**

```
array.push(element1, element2, element, ... , elementN )
```

[数组长度](https://www.geeksforgeeks.org/javascript-array-length-property/)方法可以用来求对应数组的长度。

**语法:**

```
array.length
```

**返回值:**数字

**示例:**

## HTML

```
<!DOCTYPE html>
<html lang="en">

<head>
    <title>
        JavaScript mapping using loops
    </title>
</head>

<body>
    <script>
        var arr = [4, 5, 10, 3, 8, 6];
        var result = [];
        let i;

        //square function returns square of a number
        const square = function(num){  
            return num*num;
        }

        for(i=0; i< arr.length; i++){
            result.push(square(arr[i]));
        }

        console.log(result);
        //Expected output: [16 ,25, 100, 9, 64, 36]

    </script>
</body>

</html>
```

**输出:**输出数组中元素的索引显示在输出中的数字以及输出数组的长度之前。

```
[16, 25, 100, 9, 64, 36]
0: 16
1: 25
2: 100
3: 9
4: 64
5: 36
length: 6
```