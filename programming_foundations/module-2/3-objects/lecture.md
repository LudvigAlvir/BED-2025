---
header: "Lesson 2.3: Objects"
marp: true
theme: default
size: 16:9
paginate: true
color: #111
backgroundColor: #eee
_footer: "@2025 Ludvig Alvir"
---

# Objects

---

## Structure

```js
const object = {
  key: "value",
};
```

---

## properties

```js
const student = {
  name: "Adrian",
  dateOfBirth: "1995-01-01",
  enrollmentDate: "2025-08-01",
  course: "BED",
};
console.log(student.name);
console.log(student["course"]);
student.course = "FED";
console.log(student.course);
```

---

## obj\[key] vs obj.key

```js
const student = {
  "first-name": "Markus",
  "last-name": "Olsen",
};
console.log(student["first-name"]);
console.log(student.first - name);
```

- Data from API's

---

## Looping over objects

```js
for (const key in object) {
  console.log(key);
}
```

---

## Looping over objects

```js
for (const key in object) {
  console.log(object[key]);
}
```

---

## Methods

```js
const student = {
  name: "Adrian",
  course: "FED",
  changeCourse: function (course) {
    this.course = course;
  },
};
console.log(student.course);
student.changeCourse("BED");
console.log(student.course);
```
