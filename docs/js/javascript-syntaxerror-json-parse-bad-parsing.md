# JavaScript 语法错误–JSON . parse:bad parsing

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-JSON-parse-bad-parsing/](https://www.geeksforgeeks.org/javascript-syntaxerror-json-parse-bad-parsing/)

如果作为参数传递给方法的字符串无效，就会出现由 **JSON.parse()** 引发的这个 JavaScript 异常。

**消息:**

```
SyntaxError: JSON.parse: unterminated string literal
SyntaxError: JSON.parse: bad control character in string literal
SyntaxError: JSON.parse: bad character in string literal
SyntaxError: JSON.parse: bad Unicode escape
SyntaxError: JSON.parse: bad escape character
SyntaxError: JSON.parse: unterminated string
SyntaxError: JSON.parse: no number after minus sign
SyntaxError: JSON.parse: unexpected non-digit
SyntaxError: JSON.parse: missing digits after decimal point
SyntaxError: JSON.parse: unterminated fractional number
SyntaxError: JSON.parse: missing digits after exponent indicator
SyntaxError: JSON.parse: missing digits after exponent sign
SyntaxError: JSON.parse: exponent part is missing a number
SyntaxError: JSON.parse: unexpected end of data
SyntaxError: JSON.parse: unexpected keyword
SyntaxError: JSON.parse: unexpected character
SyntaxError: JSON.parse: end of data while reading object contents
SyntaxError: JSON.parse: expected property name or '}'
SyntaxError: JSON.parse: end of data when ',' or ']' was expected
SyntaxError: JSON.parse: expected ',' or ']' after array element
SyntaxError: JSON.parse: end of data when property name was expected
SyntaxError: JSON.parse: expected double-quoted property name
SyntaxError: JSON.parse: end of data after property name when ':' 
             was expected
SyntaxError: JSON.parse: expected ':' after property name in object
SyntaxError: JSON.parse: end of data after property value in object
SyntaxError: JSON.parse: expected ',' or '}' after property value in 
             object
SyntaxError: JSON.parse: expected ',' or '}' after property-value 
             pair in object literal
SyntaxError: JSON.parse: property names must be double-quoted strings
SyntaxError: JSON.parse: expected property name or '}'
SyntaxError: JSON.parse: unexpected character
SyntaxError: JSON.parse: unexpected non-whitespace character after 
             JSON data
SyntaxError: JSON.parse Error: Invalid character at position {0} 
             (Edge)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**传递给 JSON.parse()方法的此字符串无效，将引发此错误。

**例 1:**

## 超文本标记语言

```
<script>
    var str = '{"Prop_1" : "Val_1"}';
    JSON.parse(str);
    document.write(str);
</script>
```

**输出:**

```
{"Prop_1" : "Val_1"}

```

**例 2:**

## 超文本标记语言

```
<script>
    var str = '{"Prop_1" : "Val_1"}}';
    JSON.parse(str);
    document.write(str);
</script>
```

**输出(控制台中):**

```
Unexpected token } in JSON at position 2

```