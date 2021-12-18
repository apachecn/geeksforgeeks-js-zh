# 类型脚本访问器

> 原文:[https://www.geeksforgeeks.org/typescript-accessor/](https://www.geeksforgeeks.org/typescript-accessor/)

在 TypeScript 中，有两种受支持的方法 getter 和 setter 来访问和设置类成员。对如何在每个对象上访问成员有更大的方法控制。
**type script 访问器属性的方法:**

*   **getter:** 当你想访问一个对象的任何属性时，这个方法就会出现。
*   **setter:** 当你想改变一个对象的任何属性时，这个方法就会出现。

**getter:** 用于提取变量的值 **getter 访问器**属性是常规方法。它由对象文字中的 **get** 关键字表示。
**语法:**

```
get accessName() {  
    // getter, the code executed on getting obj.accessName  
  },  
```

**例:**

## java 描述语言

```
class MyClass {
    private _with:number = 5;
    private _height:number = 10;
    get square() {
        return this._with * this._height;
    }
}
console.log(new MyClass().square);
```

**输出:**

```
50
```

吸气剂可以是公共的、受保护的、私有的。让某物表现得像一个属性或函数只是人为的。所以，得到 square()和新的 MyClass()。square 与 square()和 new MyClass()相同。正方形()。
**Setter:** 为了更新变量的值， **setter 访问器**属性是使用的常规方法。它们由对象文字中的 **set** 关键字表示。
**语法:**

```
set accessName(value) {  
    // the code executed on setting 
    //obj.accessName = value, from setter  
  }  
```

**例:**

## java 描述语言

```
set fullname {
    const parts = value.split ('');
    this.partname = firstname[0];
    this.partname = firstname[1];
}
person fullname = "Hitangshu Agarwal"
console.log(person);
```

**输出:**

```
firstname: "Hitangshu"
lastname: "Agarwal"
```

下面的例子清楚地说明了吸气剂和设置剂的概念:
**例子:**

## java 描述语言

```
const company = {
    companyName = "GeeksforGeeks",
    companyTag = "Edutech",

    // Function that return the Full description
    // combined both comapnyName and companyTag
    get full_Desc () {
        return `${company.companyName} ${company.CompanyTag}`
    },

    // It will return separately companyName and companyTag
    set full_Desc(value) {
        const parts = value.split ('');
        this.partname = companyName[0];
        this.partname = CompanyTag[1];
    }
};

company.full_Desc = "GeeksforGeeks Edutech";
console.log(company);
```

**输出:**

```
GeeksforGeeks Edutech
```

**要记住的点:**

*   借助于 **getter** 和 **setter** ，我们实现了对如何在每个对象上访问成员的适当控制。
*   typescript 访问器需要将编译器设置为输出 ECMAScript 5 或更高版本我们应该需要 TypeScript 访问器。它不支持低于 ECMAScript 5 的版本。
*   带有 get 和 no set 属性的访问器被自动假定为只读的，不需要手动操作。当我们从代码中生成一个**d . ts**文件时，这很有帮助。