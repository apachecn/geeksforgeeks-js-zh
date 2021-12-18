# 如何用 JavaScript 获取字符串的前三个字符？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 获取字符串的前三个字符/](https://www.geeksforgeeks.org/how-to-get-the-first-three-characters-of-a-string-using-javascript/)

下面的方法介绍了如何找到字符串的 3 个字母，这里我们将使用给定日期的 JavaScript 将日期名称作为字符串。

**例:**

```
Input: today
Output: SUN

Input: tomorrow
Output: MON

Input: yesterday
Output: SAT

Input: 01-04-2021
Output: THU
```

**方法:**

*   First, use **new date ()** to get the current date and store it in the variable ( **date** ).
*   If the input date is tomorrow, use the **setting date** () method to increase a date to **date ()** , and if the input date is yesterday, decrease a date from **date ().**
*   If the value is not today's **, then we will pass the entered date to the **date ()** object. That is why if the user inputs **today** , then the date () will be the default, and the default date () object describes today's date ().**
***   Now we get the date by using the **date. getday ()** method. It will return a number between 0 and 6, where 0 represents **Sunday** , 6 represents **Saturday** , and the remaining days are arranged in order. Create an array containing the day of the week. Use the index to get the preferred date name.*   Extract the first three characters by slicing.**

****示例:**创建一个 **index.js** 文件，并写下以下代码。**

**<gfg-tab role="tab" slot="tab" id="gfg-tab-0"><gfg-panel role="tabpanel" slot="panel" id="gfg-panel-0" data-code-lang="javascript"></gfg-panel></gfg-tab>**

```
`<script>
// Javascript program to get three  beginning characters of the day

function getDay(d) {
    let date = new Date();
    let days = ["SUNDAY", "MONDAY", "TUESDAY", "WEDNESDAY",
        "THURSDAY", "FRIDAY", "SATURDAY"]

    if (d === "tomorrow") {
        date.setDate(date.getDate() + 1)
    } else if (d === "yesterday") {
        date.setDate(date.getDate() - 1)
    } else if (d != "today") {
        date = new Date(d);
    }

    // Get the todays day
    let day = days[date.getDay()]

    // Extract three characters from the beginning
    let threeCharDay = day.slice(0, 3)

    // Print or return the three character day
    console.log(threeCharDay)
}

// Function calls
getDay("yesterday")
getDay("today")
getDay("tomorrow")
getDay("2021-03-30")
getDay("2021-03-31")
getDay("2021-04-01")
</script>`
```