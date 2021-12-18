# YAML 和 JSON 有什么区别？

> 原文:[https://www . geesforgeks . org/YAML 和-json 的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-yaml-and-json/)

**YAML:** 这是一种轻量级的、人类可读的数据表示语言。它主要是为了使格式易于阅读，同时包含复杂的功能。由于 YAML 是 JSON 的超集，它可以用 YAML 解析器解析 JSON。YAML 的分机是**。yaml** 或**。yml** 。YAML 规范允许用户定义数据类型以及显式数据类型。

**YAML 最常用的数据类型有:**

*   figure
*   character string
*   null value
*   Boole
*   And date and time stamp.
*   sequence
*   Nested value

**例:**

```
Origin:
   author: Dan Brown
   language: English
   publication-date: 2017-10-03
   pages: 461
   description: | When billionaire researcher Edmond Kirsch is killed, 
                  it is up to Robert Langdon & Ambra Vidal to honor 
                  his memory by making public his findings concerning the 
                  origin of human life and its destiny.

```

**[JSON:](https://www.geeksforgeeks.org/json-full-form/)** 它是一种独立于语言、人类可读的语言，因其简单而被使用，最常用于基于网络的应用程序。JSON 扩展以**结尾。json** 。JSON 是 XML 的用户友好的替代品，因为它重量轻，易于阅读。

**JSON 中使用的一些有效数据类型有:**

*   figure
*   character string
*   target
*   array

**例:**

```
{
  "Origin": {
    "author": "Dan Brown",
    "language": "English",
     "publication-date": "2017-10-03",
     "pages": 461,
     "description": "When billionaire researcher Edmond Kirsch is killed, 
                     it is up to Robert Langdon and Ambra Vidal to honor
                     his memory  by making public his findings concerning 
                     the origin of human life and its destiny."
  }
}

```

**YAML 和 JSON 的区别是:**T32】T33

| [亚姆语] | JSON |
| Comments are represented by hash/numeric symbols. | No comment allowed. |
| Levels are represented by double space characters. Tabs are not allowed. | Objects and arrays are represented by braces and brackets. |
| String quotation marks are optional, but single and double quotation marks are supported. | String must be enclosed in double quotation marks. |
| The root can be any valid data type. | The root node must be an array or object. |