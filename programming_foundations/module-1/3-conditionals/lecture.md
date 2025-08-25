---
header: "Lesson 1.3: Conditionals"
marp: true
theme: default
size: 16:9
paginate: true
color: #111
backgroundColor: #eee
_footer: "@2025 Ludvig Alvir"
---

# Conditionals

---

## Decisions can be based on information

```
If it's warm outside:
    Wear shorts
If it's cold outside:
    Wear pants
```

---

## if/else

```
If it's warm outside:
    Wear shorts
else:
    Wear pants
```

---

## Defining cases

```js
let temperature = 22;
if (temperature > 20) {
  console.log("Wear shorts");
}
if (temperature < 20) {
  console.log("Wear pants");
}
```

---

## Mistakes that will happen

```js
let temperature = 20;
if (temperature > 20) {
  console.log("Wear shorts");
}
if (temperature < 20) {
  console.log("Wear pants");
}
```

```js
let temperature = 20;
if (temperature >= 20) {
  console.log("Wear shorts");
}
if (temperature <= 20) {
  console.log("Wear pants");
}
```

---

## else if

```js
let temperature = 20;

if (temperature > 20) {
  console.log("Wear shorts");
} else if (temperature < 20) {
  console.log("Wear pants");
} else {
  console.log("Fallback value"); // Could be wear pants
}
```

---

## Blocks{}

- Outer/Inner
- Values are lost when scope is done
- Can redeclare ("shadowing", more intermidiate)

---

## Example

```js
const statement = true;
if (statement) {
  let value = 10;
}
console.log(value);
```

---

## Example

```js
const x = 10;
{
  const x = 20;
  console.log(x);
}
console.log(x);
```

---

## Why we don't use var

```js
var x = 10;
{
  var x = 20;
  console.log(x);
}
console.log(x);
```

---

## Truthy and falsy

Rule of thumb:

- values are truthy
- no value is falsy

---

## Exceptions and testing

```js
if (0) {
  console.log("0 was a truthy statement");
} else {
  console.log("0 was a falsy statement");
}

if ("0") {
  console.log('"0" was a truthy statement');
} else {
  console.log('"0" was a falsy statement');
}
```

---

## Ternary

There is a "shortcut" to write if/else statements in js.

```js
const number = 10;
let result;
if (num > 5) {
  result = "big umber";
} else {
  result = "small number";
}
```

```js
let number = 10;
let result = num > 5 ? "big number" : "small number";
console.log(result);
```

---

## Switch statements

Large if/else statements.

```js
let key = user.input();

switch (key) {
  case "left":
    console.log("left key pressed");
    break;

  case "right":
    console.log("right key pressed");
    break;
}
```

---

## For loops

```js
for (let index = 0; index < 10; index++) {
  console.log(index);
}
```

---

## For loops

What will be the difference?

```js
let index = 0;
for (; index < 10; index++) {
  console.log(index);
}
```

---

## For loops

What will be the difference?

```js
for (let index = 0; index < 10; ) {
  console.log(index);
  index++;
}
```

---

## For loops (standard)

```js
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

---

## While loops

```js
let i = 0;
while (i < 10) {
  console.log(i);
  i++;
}
```

---

## Jump statements

- continue
- break
