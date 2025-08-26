---
header: "Lesson 2.2: Functions"
marp: true
theme: default
size: 16:9
paginate: true
color: #111
backgroundColor: #eee
_footer: "@2025 Ludvig Alvir"
---

# Functions

---

## Reusability

```js
function begForSubs() {
  console.log("Thank you for watching my video!");
  console.log("Please like, comment and subscribe!");
}
```

---

## Anatomy of a function

```js
function functionName(parameter1, parameter2) {
  let value = "something";
  // do something
  return value;
}
console.log(functionName("argument1", "argument2"));
```

---

## Example function

```js
function greetUser(name) {
  alert("Welcome " + name + "!");
}
greetUser("Carl");
```

---

## Default values

```js
function greetUser(name = "Ola") {
  alert("Welcome " + name + "!");
}
greetUser();
```

---

## Spread operator

```js
function sortNames(...args) {
  return args.sort();
}
```

---

## Reusability

```js
const input = Number(prompt("Guess a number between 1 and 10"));
if (input === parseInt(Math.random() * 10 + 1)) {
  alert("guessed correctly!");
} else {
  alert("guessed wrong!");
}
```

---

## Reusability

```js
const input = getNumberFromUser();
guessNumber(input);
```

---

## "Hide" logic

```js
function calculateHypotenuse(a, b) {
  if (
    typeof a === "number" &&
    !isNaN(a) &&
    typeof b === "number" &&
    !isNaN(b)
  ) {
    return Math.sqrt(a ** 2 + b ** 2);
  } else {
    throw new error("invalid arguments");
  }
}

const sideX = 3;
const sideY = 4;
const hypotenuse = calculateHypotenuse(sideX, sideY);
console.log(hypotenuse);
```

---

## Making the code easier to read

```js
function calculateHypotenuse(a, b) {
  if (
    typeof a === "number" &&
    !isNaN(a) &&
    typeof b === "number" &&
    !isNaN(b)
  ) {
    return Math.sqrt(a ** 2 + b ** 2);
  } else {
    throw new error("invalid arguments");
  }
}
```

---

## Functions as values

```js
const sum = function (a, b) {
  return a + b;
};
console.log(sum(2, 4));
```

---

## Arrow functions

```js
const functionName = () => {
  console.log("Function called");
};
functionName();
```

---

## Callback functions

Anonymous callback functions

```js
const students = ["Markus", "Herman", "Adrian"];
students.forEach((item) => {
  console.log(item);
});
```

---

## Creating interactive sites
