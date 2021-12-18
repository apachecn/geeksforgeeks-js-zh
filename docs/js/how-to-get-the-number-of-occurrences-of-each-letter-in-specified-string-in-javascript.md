# 如何在 JavaScript 中获取指定字符串中每个字母的出现次数？

> 原文:[https://www . geeksforgeeks . org/如何获取 javascript 中指定字符串中每个字母的出现次数/](https://www.geeksforgeeks.org/how-to-get-the-number-of-occurrences-of-each-letter-in-specified-string-in-javascript/)

给定一个字符串，我们的任务是在用户定义函数的帮助下找到字符串中某个字符的出现。

```
Example:
Input : "hello"
Output : h occur 1 times
         e occur 1 times
         l occur 2 times
         o occur 1 times
Explanation : here "hello" have 1 h, so it have 1 value.
               as same e have 1, l have 2 , o have 1.
Example 2:
Input : "did"
Output: d occur 2 times 
        i occur 1 times
```

**方法 1:** 在这种方法中，我们使用地图数据结构来存储字符出现的次数。

*   首先，我们用键初始化映射字符串的每个字符，每个字符的值为 0。
*   我们迭代字符串并增加字符的值。
*   最后，打印地图的键值。

**示例:**

## java 描述语言

```
<script>

//function to print occurrence of character
function printans( ans )
{
  for( let [ key ,value] of ans)
  {
    // if()
    console.log(`${key}  occurs  ${value} times` );

  }

}

// function count occurrence of character
function count( str , outp_map )
{
  for( let i = 0 ;i < str.length ;i++)
  {

    let k = outp_map.get(str[i]);
    outp_map.set(str[i], k+1) ;

  }
  //calling  print function
  printans(outp_map);
}

//function create map to count character
function count_occurs( test , callback )
{
  //checking string is valid or not
  if( test.length === 0 )
  {
    console.log(" empty string ");
    return ;
  }
  else
  {
    // map for storing count values
    let ans = new Map();
    for( let i = 0 ;i < test.length;i++)
    {
      ans.set(test[i], 0);
    }

    callback( test ,ans);

  }

}

// test string
let test =  "helloworld";
count_occurs( test ,count);

</script>
```

**输出:**

```
h  occurs  1 times
e  occurs  1 times
l  occurs  3 times
o  occurs  2 times
w  occurs  1 times
r  occurs  1 times
d  occurs  1 times
```

**方法 2:** 在这种方法中，我们使用嵌套 for 循环对字符串进行迭代，并对字符串中的每个字符进行计数。

*   首先用字符串的值初始化*值为 0 的计数。*
*   现在我们遍历字符串，如果带有值的*与字符匹配，则将计数值增加 1。*
*   最后，打印计数的值。

**示例:**

## java 描述语言

```
<script>

// function that count character occurrences in string
function count_occur( str )
{
  // checking string is valid or not
  if( str.length == 0 )
  {
    console.log("Invalid string")
    return;
  }
  //cor loop to iterate over string
  for( let i = 0 ;i < str.length ;i++)
  {
    //variable counting occurrence
    let count = 0;
    for( let j = 0 ;j < str.length ;j++)
    {
      if( str[i] == str[j] && i > j  )
      {
       break;
      }
      if( str[i] == str[j]  )
      {
        count++;
      }
    }
    if( count > 0)
    console.log(`${str[i]} occurs ${count} times`);

  }

}

// test string
let test_str = "gfghello";
count_occur( test_str);
</script>
```

**输出:**

```
g occurs 2 times
f occurs 1 times
h occurs 1 times
e occurs 1 times
l occurs 2 times
o occurs 1 times
```