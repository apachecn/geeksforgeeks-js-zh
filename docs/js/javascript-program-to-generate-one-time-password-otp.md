# JavaScript |程序生成一次性密码(OTP)

> 原文:[https://www . geesforgeks . org/JavaScript-程序生成一次性密码-otp/](https://www.geeksforgeeks.org/javascript-program-to-generate-one-time-password-otp/)

一次性密码是一种仅在计算机或数字设备上的一次登录会话或事务中有效的密码。如今，OTP 几乎被用于每一项服务，如网上银行、网上交易等。它们通常是 4 或 6 位数字或 6 位字母数字的组合。随机函数用于生成在数学库中预定义的随机动态口令。本文描述了如何使用 JavaScript 生成动态口令。

**已用功能:**

*   **Math.random():** 此函数返回 0 到 1 之间的任意随机数。
*   **Math.floor():** 将任意浮点数的 floor 返回整数值。

使用上面的函数选择一个随机的字符串数组索引，它包含了动态口令特定数字的所有可能的候选者。

**示例 1:** 本示例生成 4 位数字 OTP:

```
<script>

// Function to generate OTP
function generateOTP() {

    // Declare a digits variable 
    // which stores all digits
    var digits = '0123456789';
    let OTP = '';
    for (let i = 0; i < 4; i++ ) {
        OTP += digits[Math.floor(Math.random() * 10)];
    }
    return OTP;
}

document.write("OTP of 4 digits: ")
document.write( generateOTP() );
</script>                    
```

**输出:**

```
OTP of 4 digits: 2229
```

**示例 2:** 本示例生成 6 位数字 OTP:

```
<script>

// Function to generate OTP
function generateOTP() {

    // Declare a digits variable 
    // which stores all digits
    var digits = '0123456789';
    let OTP = '';
    for (let i = 0; i < 6; i++ ) {
        OTP += digits[Math.floor(Math.random() * 10)];
    }
    return OTP;
}

document.write("OTP of 6 digits: ")
document.write( generateOTP() );
</script>                    
```

**输出:**

```
OTP of 6 digits: 216664
```

**示例 3:** 本示例生成长度为 6:

```
<script>

// Function to generate OTP
function generateOTP() {

    // Declare a string variable 
    // which stores all string
    var string = '0123456789abcdefghijklmnopqrs
    tuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
    let OTP = '';

    // Find the length of string
    var len = string.length;
    for (let i = 0; i < 6; i++ ) {
        OTP += string[Math.floor(Math.random() * len)];
    }
    return OTP;
}

document.write("OTP of 6 length: ")
document.write( generateOTP() );
</script>                    
```

**输出:**

```
OTP of 6 length: rab0Tj
```