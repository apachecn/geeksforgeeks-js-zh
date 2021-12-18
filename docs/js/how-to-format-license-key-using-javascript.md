# 如何使用 JavaScript 格式化许可证密钥？

> 原文:[https://www . geesforgeks . org/how-format-license-key-use-JavaScript/](https://www.geeksforgeeks.org/how-to-format-license-key-using-javascript/)

给定一个字符串，任务是将该字符串格式化为许可证密钥。

**规则:**

*   输入字符串包含字母数字字符和破折号
*   输入字符串由 N+1 组用 N 个破折号隔开。
*   输出字符串必须用破折号按 K 个字符分组。
*   第一组可以少于 K 个字符，但不能为零。
*   输出字符串不得包含任何小写字符。

您已经给出了输入字符串**字符串**和数字 **K**

**示例:**

```
Input:  str = "dsf354g4dsg1"
          k = 4
Output: "DSF3-54G4-DSG1"

Input:  str = "d-sf354g4ds-g1dsfgdf-sfd5ds65-46"
        k = 6
Output:  "D-SF354G-40DSGS-FGFSFD-DS6546"

Input:  str = "   d-sf354';.;.';.'...,k/]gcs-hsfgdf-sfs6-46"
Output:   k = 5

Output: "DS-F354K-GCSHS-FGDFS-FS646"
```

为了解决这个问题，我们使用以下步骤:

*   创建一个接受两个参数 **str** 和 **k** 的函数。
*   使用 [**String.trim()**](https://www.geeksforgeeks.org/javascript-string-prototype-trim-function/) 方法删除前导空格和结尾空格。
*   使用 [**String.replace()**](https://www.geeksforgeeks.org/javascript-string-replace-method/) 方法并用 regex **/[^a-zA-Z0-9]/g** 搜索来替换所有特殊字符。
*   使用[**string . touppercase()**](https://www.geeksforgeeks.org/javascript-string-touppercase/)**方法将字符串转换为大写。**
*   **使用[**string . split()**](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/)**方法将字符串转换为数组。现在，str 是一个数组，其中所有的元素都是大写字符和数字(以字符串的形式)。****
*   ****使用 for 循环并用 str 的长度初始化循环并运行它，直到 **i** 大于 0，并且在每次迭代之后， **i** 的值减少 **k.** 基本上，我们想要一个从 str 的背面运行的循环。****
*   ****现在在每次迭代时用破折号“-”连接字符串****
*   ****现在在 str 上使用[**array . join()**](https://www.geeksforgeeks.org/javascript-array-join-method/)**方法将 str 转换成 String 并从函数中返回字符串。******

## ******java 描述语言******

```
****<script>
    function format(str, k) {
        str = str

            // Remove the white spaces
            .trim()

            // Replace all the special
            // characters with ""
            .replace(/[^a-zA-Z0-9]/g, "")

            // Transform the string into
            // uppercase characters
            .toUpperCase()

            // Convert the string into array
            .split("");

        // Store the length of the
        // array into len
        let len = str.length;

        for (let i = len; i > 0; i = i - k) {
            if (i != len) {

                // Concatenate the string with "-"
                str[i - 1] = str[i - 1] + "-";
            }
        }

        //  Join the array to make it a string
        return str.join("");
    }

    console.log(format("dsf354g4dsg1", 4))
    console.log(format(
        "d-sf354g40ds-gsfgf-sfdds65-46", 6))
    console.log(format(
"   d-sf354';.;.';.'...,k/]gcs-hsfgdf-sfs6-46", 5))
</script>****
```

********输出:********

```
****"DSF3-54G4-DSG1"**

**"D-SF354G-40DSGS-FGFSFD-DS6546"**

**"DS-F354K-GCSHS-FGDFS-FS646"****
```