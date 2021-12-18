# 如何在 JavaScript 中检查传递的字符串是否是回文？

> 原文:[https://www . geesforgeks . org/如何检查传递的字符串是否是 javascript 中的回文/](https://www.geeksforgeeks.org/how-to-check-whether-a-passed-string-is-palindrome-or-not-in-javascript/)

给定一个字符串，我们的任务是找出字符串是不是回文。

```
Example:
Input : "race"
Output : passed string is not a palindrome
Explanation : if we write "race" in reverse that is "ecer" it not 
matches with first string so it is not a pallindrome.
Example 2:
Input : "hellolleh"
Output : passed string is palindrome.
```

**方法 1:** 在这种方法中，我们使用以下步骤。

*   首先，我们向前和向后迭代一个字符串。
*   检查所有向前和向后的字符是否匹配，返回 true。
*   如果所有向前和向后字符不匹配，则返回 false。
*   如果返回是真的，那就是回文。

**例:**

## java 描述语言

```
<script>
  // function that check str is palindrome or not
  function check_palindrome( str )
  {
    let j = str.length -1;
    for( let i = 0 ; i < j/2 ;i++)
    {
      let x = str[i] ;//forward character
      let y = str[j-i];//backward character
      if( x != y)
      {
        // return false if string not match
        return false;
      }
    }
    /// return true if string is palindrome
    return true;

  }

  //function that print output is string is palindrome
  function is_palindrome( str )
  {
    // variable that is true ig string is pallindrome
    let ans = check_palindrome(str);
    //condition checking ans is true or not
    if( ans == true )
    {
      console.log("passed string is palindrome ");
    }
    else
    {
      console.log("passed string not a palindrome");
    }
  }
  // test variable
  let test = "racecar";
  is_palindrome(test);
</script>
```

**输出:**

```
passed string is palindrome.
```

**方法 2:** 另一种方法是反转字符串，检查初始字符串是否与反转字符串匹配。

请遵循以下步骤:

*   初始化 *revese_str* 一个变量，该变量存储传递的字符串的反码。
*   将该字符串与 *reverse_str* 进行比较。
*   如果匹配，就是回文。
*   否则字符串不是回文。

**示例:**

## java 描述语言

```
<script>
  // function to reverse the string
  function reverse( str )
  {
    // variable holds reverse string
    let rev_str = "";
    for( let i = str.length-1 ;i >= 0 ;i--)
    {
      rev_str+= str[i];
    }
    // return reverse string
    return rev_str;
  }

  //  function checking string is palindrome or not
  function is_palindrome( str )
  {
    reverse_str = reverse(str);
    //  condition checking if reverse str is
    // same as string it is palindrome
    // else not a palindrome
    if( reverse_str === str)
    {
      console.log("passed string is palindrome ");
    }
    else
    {
      console.log("passed string is not palindrome")
    }
  }
  let test = "hellolleh";
  is_palindrome(test);
</script>
```

**输出:**

```
passed string is palindrome.
```