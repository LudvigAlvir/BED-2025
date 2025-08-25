---
header: "Lesson 1.4: Arrays "
marp: true
theme: default
size: 16:9
paginate: true
color: #111
backgroundColor: #eee
_footer: "@2025 Ludvig Alvir"
---

# Arrays

---

## Grouping similar items

```js
let student1 = "Adrian";
let student2 = "Markus";
let student3 = "Henrik";
```

---

## Grouping similar items

```js
const students = ["Adrian", "Markus", "Henrik"];
```

---

## Mixing

```js
const mixedArray = [1, true, undefined, "Henrik", ["Markus", "Adrian"]];
```

---

## 0 based indexing

```js
const students = ["Adrian", "Markus", "Henrik"];
console.log(students[0]);
console.log(students[2]);
console.log(students[3]);
```

---

## Changing arrays

```js
const students = ["Adrian", "Markus", "Henrik"];
students.push("Herman");
console.log(students);
```

---

## Changing arrays

- push
- pop
- shift
- unshift

---

## Changing arrays

- slice
- splice

---

## Const for arrays (reference)

```js
let letArray = [1, 2, 3];
const constArray = [4, 5, 6];
letArray.push(10);
constArray.push(10);
letArray = [1, 2];
constArray = [4, 5]; // error
```

---

## Reference

```js
const arr = [1, 2, 3];
const copy = arr;
arr[0] = 4;
console.log(copy);
```

---

## Looping over arrays

What will be the output

```js
const arr = [5, 4, 3, 2, 1];
for (let i = 0; i < 10; i++) {
  console.log(arr[i]);
}
```

---

## Looping over arrays

why < and not <=?

```js
const arr = [5, 4, 3, 2, 1];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

---

## Looping over arrays

```js
const arr = [5, 4, 3, 2, 1];

let i = 0;
while (i < arr.length) {
  console.log(arr[i]);
  i++;
}
```

---

## Copying

Shallow copy

```js
const arr = [1, 2, 3];
const copy = [...arr];
arr[0] = 10;
console.log(copy);
```

---

## Copying

Deep copy

```js
const arr = [1, 2, 3];
const copy = JSON.parse(JSON.stringify(arr));
arr[1] = 0;
console.log(copy);
```

---

## Multi dimension arrays

```js
const multiDimensionalArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
];
console.log(multiDimensionalArray[0][0]);
console.log(multiDimensionalArray[1][1]);
```
