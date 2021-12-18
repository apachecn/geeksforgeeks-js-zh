# 如何在 JavaScript 中以字符串格式获取明天的日期？

> 原文:[https://www . geesforgeks . org/how-to-to-tomorrow-字符串格式日期-javascript/](https://www.geeksforgeeks.org/how-to-get-tomorrows-date-in-a-string-format-in-javascript/)

在本文中，我们将看到如何使用 JavaScript 以字符串形式打印明天的日期。

为了实现这一点，我们使用日期对象并创建它的一个实例。之后，通过使用 setDate()方法，我们将一个日期增加到当前日期。现在，通过使用 getDate()方法，您将获得明天的日期。现在要将该日期转换为字符串，我们使用字符串模板文字、getFullYear、getMonth、padStart 方法。以下是这方面的实施情况:

**例:**

## Javascript

```
<script>
    const tomorrow = () => {

        // Creating the date instance
        let d = new Date();

        // Adding one date to the present date
        d.setDate(d.getDate() + 1);

        let year = d.getFullYear()
        let month = String(d.getMonth() + 1)
        let day = String(d.getDate())

        // Adding leading 0 if the day or month
        // is one digit value
        month = month.length == 1 ? 
            month.padStart('2', '0') : month;

        day = day.length == 1 ? 
            day.padStart('2', '0') : day;

        // Printing the present date
        console.log(`${year}-${month}-${day}`);
    }

    tomorrow()
</script>
```

**输出:**

```
"2021-03-28"
```

#### 例 2:

#### 如果给出了日期:

## java 描述语言

```
<script>
    const tomorrow = (dt) => {

        // Creating the date instance
        let d = new Date(dt);

        // Adding one date to the present date
        d.setDate(d.getDate() + 1);

        let year = d.getFullYear()
        let month = String(d.getMonth() + 1)
        let day = String(d.getDate())

        // Adding leading 0 if the day or month
        // is one digit value
        month = month.length == 1 ? 
            month.padStart('2', '0') : month;

        day = day.length == 1 ? 
            day.padStart('2', '0') : day;

        // Printing the present date
        console.log(`${year}-${month}-${day}`);
    }

    tomorrow("2020-12-31")
    tomorrow("2021-02-28")
    tomorrow("2021-4-30")
</script>
```

**输出:**

```
"2021-01-01"
"2021-03-01"
"2021-05-01"
```

**注意:**以 yyyy-mm-dd 格式输入日期。