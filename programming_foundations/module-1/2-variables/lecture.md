---
header: "Lesson 1.2: Variables, operators and logic"
marp: true
theme: default
size: 16:9
paginate: true
color: #111
backgroundColor: #eee
_footer: "@2025 Ludvig Alvir"
---

# Variables, Operators and Logic

---

## Data types

```js
let age = 21; // Numbers
let name = "Ola"; // Strings
let isAdult = true; // Boolean
let noValueSetYet; // undefined
let onPurpose = null; // null (object) intentional
let array = [1, 2, 3]; // array
let object = { key: "value" }; // object
```

---

## Variables

```js
var first = "var";
let second = "let";
const third = "const";
```

---

## Semicolons ( ; )

Ends a line

---

## Type coercion

```js
1 + 1; // 2
"hello" + " " + "world"; // hello world
1 + "1"; // ?
```

---

## typeof

```js
typeof "text";
typeof 10;
typeof false;
typeof undefined;
typeof null;
```

Try yourself to get used to types.
We can use it to validate data later.

---

## Naming things

**The hardetst part of programming**

- camelCase
- PascalCase
- snake_case
- UPPER_SNAKE
- kebab-case (HTML/CSS: Not js)

---

## Naming things

```js
let age = 21; // valid
let _isActive = true; // valid
let $resultContainer; // valid
let 2example = 10 // invalid
let hello world = "hello world" // invalid
```

---

## Operators

| Operator | name                | example  | result        |
| -------- | ------------------- | -------- | ------------- |
| +        | additions           | 3 + 4    | 7             |
| -        | subtraction         | 8 - 2    | 6             |
| \*       | multiplication      | 2 \* 3   | 6             |
| /        | division            | 8 / 4    | 2             |
| %        | modulus (remainder) | 5 % 2    | 1             |
| \*\*     | exponentiation      | 2 \*\* 3 | 8             |
| ++       | increment           | x++      | 1 more than x |
| --       | decrement           | x--      | 1 less than x |

---

## Using the console

```js
console.log("hello world");
console.log(1 + 3);
console.log(9 / 3);
```

---

## Operator precedence

```js
console.log(2 + 5 * 4);
console.log((2 + 5) * 4);
```

Parentheses can avoid bugs and confusion

---

## Shorthand

```js
let x = 1;
x++; // x is now 2
x--; // x is now 1
x += 2; // x is now 3
x *= 2;
console.log(x);
```

---

## Collecting inputs

```js
let name = promt("What's your name");
alert("Hello " + name + "!");
```

---

## Collecting numbers

```js
let number1 = promt("Enter the first number");
let number2 = promt("Enter the second number");
let result = number1 + number2;
alert("Result: " + result);
```

---

## Collecting numbers

```js
let number1 = promt("Enter the first number");
let number2 = promt("Enter the second number");
let result = Number(number1) + Number(number2);
alert("Result: " + result);
```

---

## Operators on non-numbers

```js
console.log("5" - 2); // 3: "5" becomes number 5
console.log("5" + 2); // "52": string + number = string concatenation
console.log("5" * "2"); // 10: both strings are coerced to numbers
console.log("5" * "two"); // NaN: "two" can’t be converted to a number
console.log("5" - "oops"); // NaN: again, "oops" isn't a number
console.log("" + 1 + 0); // "10": empty string + number = string
console.log("10" / 2); // 5: division coerces string to number
console.log("ten" / 2); // NaN: "ten" can’t be turned into a number
console.log(undefined + 1); // NaN: undefined is not numeric
```

---

## Comparison

| operator | description           |
| -------- | --------------------- |
| ==       | equal                 |
| ===      | strict equal          |
| !=       | not equal             |
| !==      | strict not equal      |
| >        | greater than          |
| <        | less than             |
| >=       | greater than or equal |
| <=       | less than or equal    |

---

## Comparison

```js
console.log(5 > 3); // true: 5 is greater than 3
console.log(2 < 1); // false: 2 is not less than 1
console.log(10 >= 10); // true: 10 is equal to 10, so "greater than OR equal" is true
console.log(7 < 7); // false: 7 is not less than 7
```

---

## Muliple comparisons

&& = AND
|| = OR
! = NOT

---

## Muliple comparisons

```js
console.log(5 > 3 && 10 > 7); // true: both comparisons are true
console.log(5 > 3 && 10 < 7); // false: the second comparison is false

console.log(5 > 3 || 10 < 7); // true: at least one comparison is true
console.log(2 > 3 || 1 > 4); // false: both are false

console.log(!true); // false: "not true"
console.log(!false); // true: "not false"
```
