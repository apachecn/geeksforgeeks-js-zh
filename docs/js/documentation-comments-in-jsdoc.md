# JSdoc 中的文档注释

> 原文:[https://www . geesforgeks . org/documentation-comments-in-jsdoc/](https://www.geeksforgeeks.org/documentation-comments-in-jsdoc/)

在 JSDoc 中，我们需要在代码中包含文档注释，JSDoc 将通过这些注释生成一个 HTML 文档网站。让我们看看如何为不同类型的代码创建文档注释。

**字符串、数字&数组:**

## Javascript

```
/**
 * Site Name
 * @type {string}
 */
const siteName = "GeeksForGeeks";

/**
 * Number
 * @type {number}
 */
const number = 1000;

/**
 * Array
 * @type {Array<number>}
 */
const myArray = [10, 20, 30];
```

在这里，我们生成了简单的 JSDoc 注释，其中描述了变量及其数据类型，并借助于 **@type** 标签进行了标注。

**物体:**

## 【JavaScript】

```
/**
 * Site object
 * @type {{id: number, name: string, rank: number|string}}
 */
const site = {
  id: 1,
  name: "gfg",
  rank: 1,
};
```

在上面的注释中，我们指定了对象的所有属性的类型。

**功能/方法:**

## Javascript

```
/**
 * Calculate age
 * @param {number} current Current year
 * @param {number} yearOfBirth Year of Birth
 * @returns {string} your calculated age
 */
const calcAge = (current, yearOfBirth) => {
  return `${current - yearOfBirth}`;
};
```

这里 **@param** 标签用于记录函数的不同参数，而**@ return**标签记录函数的返回值

**类:**

## Javascript

```
/**
 * Class to create new owner
 */
class Owner {
  /**
   * Owner details
   * @param {Object} ownerDetail
   */
  constructor(ownerDetail) {
    /**
     * @property {string} name Owner name
     */
    this.name = ownerDetail.name;

    /**
     * @property {number} age Owner's age
     */
    this.age = ownerDetail.age;
  }

  /**
   * @property {Function} printOwner Prints Owner's details
   * @returns {void}
   */
  printOwner() {
    console.log(`Owner's name is ${this.name} 
            and his age is ${this.age}`);
  }
}
```