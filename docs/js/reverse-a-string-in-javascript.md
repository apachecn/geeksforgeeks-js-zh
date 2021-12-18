# 在 JavaScript 中反转一个字符串

> 原文:[https://www . geesforgeks . org/reverse-a-string-in-JavaScript/](https://www.geeksforgeeks.org/reverse-a-string-in-javascript/)

给定一个输入字符串，任务是反转输入字符串。

**示例:**

```
Input: str = "Geeks for Geeks"
Output:  "skeeG rof skeeG"

Input: str = "Hello"
Output: "olleH"

```

在 JavaScript 中有许多方法可以反转字符串，下面将讨论其中的一些方法:

**方法 1:**

*   检查输入字符串，如果给定的字符串为空或只有一个字符，或者不是字符串类型，则返回“无效字符串”。
*   如果上述条件为 false，则创建一个数组，我们可以在其中存储结果。这里 revArray[]是新的数组。
*   从头到尾循环遍历数组，并推送数组中的每一项。
*   使用 JavaScript 中的 join()预构建函数将数组的元素连接成字符串。

**示例:**

```
<script>
function ReverseString(str) {

    // Check input
    if(!str || str.length < 2 || 
            typeof str!== 'string') {
        return 'Not valid'; 
    }

    // Take empty array revArray
    const revArray = [];
    const length = str.length - 1;

    // Looping from the end
    for(let i = length; i >= 0; i--) {
        revArray.push(str[i]);
    }

    // Joining the array elements
    return revArray.join('');
}

document.write(ReverseString("Geeks for Geeks"))
</script>
```

**输出:**

```
skeeG rof skeeG
```

**方法二:**

*   在 JavaScript 中使用 split()内置函数将字符串拆分成字符数组，即[ 'G '，' e '，' e '，' k '，' s '，' f '，' o '，' r '，' G '，' e '，' e '，' k '，' s' ]
*   在 JavaScript 中使用 reverse()函数反转字符数组，即[ 's '，' k '，' e '，' e '，' G '，' r '，' o '，' f '，' s '，' k '，' e '，' e '，' G' ]
*   在 JavaScript 中使用 join()函数将数组的元素连接成字符串。

**示例:**

```
<script>

// Function to reverse string
function ReverseString(str) {
   return str.split('').reverse().join('')
}

// Function call 
document.write(ReverseString("Geeks for Geeks"))
</script>
```

**输出:**

```
skeeG rof skeeG
```

**方法 3:**

*   使用 spread 运算符代替 split()函数将字符串转换为字符数组，即[ 'G '，' e '，' e '，' k '，' s '，' f '，' o '，' r '，' G '，' e '，' e '，' k '，' s' ]。在此了解更多关于扩散算子[扩散算子](https://www.geeksforgeeks.org/javascript-spread-operator/)
*   在 JavaScript 中使用 reverse()函数反转字符数组，即[ 's '，' k '，' e '，' e '，' G '，' r '，' o '，' f '，' s '，' k '，' e '，' e '，' G' ]
*   在 JavaScript 中使用 join()函数将数组的元素连接成字符串。

**示例:**

```
<script>
const ReverseString = str => [...str].reverse().join('');

document.write(ReverseString("Geeks for Geeks"))
</script>
```

**输出:**

```
skeeG rof skeeG
```