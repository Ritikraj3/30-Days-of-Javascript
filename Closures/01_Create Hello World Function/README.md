Here’s the README formatted version for your problem statement:

---

# 🧠 Create Hello World Function

### ✅ Solved | 🟢 Easy | 💼 Frequently Asked in Interviews

---

## 📝 Problem Statement

Write a function `createHelloWorld` that returns a **new function** which **always returns `"Hello World"`**, regardless of the arguments passed.

---

## 📥 Input

* An array `args` of any type and length between 0 and 10.

```js
0 <= args.length <= 10
```

---

## 📤 Output

A function that returns the string `"Hello World"` every time it's called.

---

## 💡 Examples

### Example 1

```js
Input: args = []
Output: "Hello World"

Explanation:
const f = createHelloWorld();
f(); // "Hello World"
```

### Example 2

```js
Input: args = [{}, null, 42]
Output: "Hello World"

Explanation:
const f = createHelloWorld();
f({}, null, 42); // "Hello World"
```

Even with arguments, the returned function always gives `"Hello World"`.

---

## 🔧 Constraints

* The function returned must **always return** the string `"Hello World"`.
* It should not be affected by the arguments passed to it.

---

## ✅ Solution (JavaScript)

```js
var createHelloWorld = function() {
  return function(...args) {
    return "Hello World";
  };
};
```

---

## 📌 Notes

* Demonstrates the concept of **closures**.
* Useful in understanding how to **return functions** from other functions.

---

