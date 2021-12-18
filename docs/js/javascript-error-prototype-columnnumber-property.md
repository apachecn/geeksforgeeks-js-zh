# JavaScript error . prototype . column number 属性

> 原文:[https://www . geesforgeks . org/JavaScript-error-prototype-column number-property/](https://www.geeksforgeeks.org/javascript-error-prototype-columnnumber-property/)

columnNumber 是非标准属性，包含引发错误的行的列号。建议不要在面向 web 的生产站点上使用此属性，因为它可能不适用于每个用户。

**使用:**该属性在创建错误对象时非常有用。如果任何错误对象的列号未定义，可以手动定义。

**语法:**

## JavaScript

```
try {
    // Creating a new error object
    var err = new Error ("Format not supported","filename",0);
    if(err.columnNumber == undefined)
        err.columnNumber = 0;
    throw err;
}
catch(e) {
    // Printing error message
    console.log ("Error: " + e.message);
    // Printing column number of line
    // at which error was raised
    console.log ("At Column number: " + e.columnNumber);
}
```