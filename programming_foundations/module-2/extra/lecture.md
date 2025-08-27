---
header: "Lesson extra: "
marp: true
theme: default
size: 16:9
paginate: true
color: #111
backgroundColor: #eee
_footer: "@2025 Ludvig Alvir"
---

# Recap

---

## Arrow functions

```js
const array = ["First", "Second", "Third"];
array.forEach((item) => {
  console.log(item);
});

window.addEventlistener("click", () => {
  console.log("user clicked");
});
```

---

## Events

```js
const btn1 = document.getElementById("btn1");
const btn2 = document.querySelector("#btn2");
btn1.onClick = () => {
  console.log("button 1 clicked");
};
btn2.addEventListener("click", () => {
  console.log("Button 2 clicked");
});
```

---

## events

```js
const btn1 = document.getElementById("btn1");
const btn2 = document.querySelector("#btn2");
function btnClick() {
  console.log("button was clicked");
}
btn1.onClick = btnClick;
btn2.addEventListener("click", btnClick);
```
