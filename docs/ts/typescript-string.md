# 类型脚本字符串

> 原文:[https://www.geeksforgeeks.org/typescript-string/](https://www.geeksforgeeks.org/typescript-string/)

在 TypeScript 中，字符串是字符值的序列，也被视为一个对象。它是一种用于存储文本数据的原始数据类型。字符串值用在单引号或双引号之间，并且字符数组的作用与字符串相同。TypeScript 字符串处理字符序列。

**语法**

```
var var_name = new String(string); 
```

**属性:**

*   **构造函数:**它将返回对字符串函数的引用。
*   **长度:**该属性将返回字符串的长度。
*   **原型:**这个属性让你添加属性和方法。

**方法:**

*   **charAt():** 该方法将返回指定索引处的字符。
*   **charCodeAt():** 此方法将返回一个数字，该数字指示指定索引处字符的 Unicode 值。
*   **concat():** 该方法将组合两个单独的字符串并返回该组合字符串。
*   **indexOf():** 它将返回索引。如果找不到，快速出现指定的值 else -1。
*   **lastIndexOf():** 它将返回索引，如果找不到指定值 else -1 的最后一次出现。
*   **localeCompare():** 该方法将返回一个数字，该数字指示引用字符串在排序顺序中位于给定字符串之前或之后，或者与给定字符串相同。
*   **match():** 该方法用于正则表达式与指定字符串的匹配。
*   **replace():** 此方法用于用正则表达式替换匹配字符串。
*   **search():** 此方法用于搜索正则表达式与指定字符串的匹配。
*   **slice():** 提取指定的字符串并返回新的字符串。
*   **split():** 将指定的 String 对象拆分为字符串数组。
*   **substr():** 从开始返回字符定义索引。
*   **substring():** 返回两个定义索引之间的字符串的字符。
*   **toLocaleLowerCase():** 该方法在尊重当前区域设置的同时将字符串转换为小写。
*   **tolocaleuppercese():**此方法将字符串转换为大写，同时考虑当前区域设置。
*   **toLowerCase():** 这个方法把字符串转换成小写。
*   **toString():** 这个方法返回一个代表指定对象的字符串。
*   **toUpperCase():** 此方法将字符串转换为大写。
*   **valueOf():** 此方法返回指定字符串的原始值。

**示例:**

```
let uname = new String("Hello geeksforgeeks");  
console.log("Message: " + uname);  
console.log("Length: " + uname.length);
```

**输出:**

```
Message: Hello geeksforgeeks
Length: 19

```

**模板字符串:**ES6 版本的 TypeScript 中的模板字符串支持。模板字符串用于将表达式固定为字符串。

**示例:**

```
let emplName:string =  "Mohit Jain";   
let compName:string = "geeksforgeeks";   
// Pre-ES6  
let emplDetail1: string = emplName + " works in the " + compName + " company.";   
// Post-ES6  
let emplDetail2: string = `${emplName} works in the ${compName} company.`;   
console.log("Before ES6: " +emplDetail1);  
console.log("After ES6: " +emplDetail2);
```

**输出:**

```
Before ES6: Mohit Jain works in the geeksforgeeks company.
After ES6:  Mohit Jain works in the geeksforgeeks company.

```

**多行字符串:** ES6 提供我们写多行字符串。这可以在下面的示例中显示。
我们必须在每个字符串的末尾添加“\n”，以便在字符串中包含一个新行。这代表了明确的说法。
**例:**

```
let multi = ' hello\n ' +  
    'Geeksforgeeks\n ' +  
    'my\n ' +  
    'name\n ' +  
    'is\n ' +  
    'Mohit Jain';  
console.log(multi);  
```

**输出:**

```
hello
Geeksforgeeks
my
name
is
Mohit Jain
```

**字符串文字类型:**它也是字符串的一种类型，字符串文字是用双引号(" ")括起来并以空值结束的字符序列。在字符串中，文字类型是一种类型，其预期值是文本内容与字符串文字类型相同的字符串。换句话说，我们可以说字符串文字允许我们指定字符串文字类型中指定的确切字符串值。当字符串文字类型使用不同的允许字符串值时，在它们之间使用“管道”或“|”符号。

**语法:**

```
Type variableName = "value1" | "value2" | "value3"; // upto N number of values  

```

字符串文字有两种用法:

*   **Variable Assignment:** Whatever the values will be allowed for literal type variable then We can assign. Otherwise, it will give the compile-time error.
    **Example:**

    ```
    type Pet = 'mouse' | 'dog' | 'Rabbit';  
    let pet: Pet;  
    if(pet = 'mouse'){  
        console.log("Correct");  
    };  
    if(pet = 'Deer')  
    {  
        console.log(" we got compilation error type!");  
    }; 
    ```

    **输出:**

    ```
    Correct
    we got compilation error type!

    ```

*   **Function Parameter:** For literal type argument we can pass only defined values. Otherwise, it will give the compile-time error.
    **Example:**

    ```
    type FruitsName = "Apple" | "Mango" | "Orange";  
    function showFruitName(fruitsName: FruitsName): void {  
        console.log(fruitsName);  
    }  
    showFruitName('Mango');   //OK - Print 'Mango'  
    //Compile Time Error  
    showFruitName('Banana');
    ```

    **输出:**

    ```
    Mango
    Banana

    ```