# JavaScript 类型错误–无法重新定义不可配置的属性“x”

> 原文:[https://www . geesforgeks . org/JavaScript-type error-cant-redefine-不可配置-property-x/](https://www.geeksforgeeks.org/javascript-typeerror-cant-redefine-non-configurable-property-x/)

这个 JavaScript 异常**不能重新定义不可配置的属性**如果用户试图重新定义一个属性，但是该属性是不可配置的，就会出现这个异常。

**消息:**T0】

**错误类型:**

```
TypeError
```

**错误原因:**如果试图重新定义属性，但该属性不可配置。

**示例 1:** 在此示例中，试图用“prop1”来更改值，因此出现了错误。

## HTML

```
<script>
var GFG_Obj = Object.create({});
Object.defineProperty(GFG_Obj, "prop1", {value: "val1"}); 
Object.defineProperty(GFG_Obj, "prop1", {value: "val2"});
</script>
```

**输出:**

```
TypeError: Cannot modify non-writable property 'prop1'
```

**示例 2:** 在此示例中，试图用“prop2”来更改值，因此出现了错误。

## HTML

```
<script>
var Obj = Object.create({"prop1": "val1"});
Object.defineProperty(Obj, "prop2", {value: "val21"}); 
Object.defineProperty(Obj, "prop2", {value: "val22"});
</script>
```

**输出:**

```
TypeError: Cannot modify non-writable property 'prop2'
```