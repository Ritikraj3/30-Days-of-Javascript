

# 🔢 Counter

### ✅ Solved | 🟢 Easy | 💼 Asked by Top Companies

---

## 📝 Problem Statement

Given an integer `n`, return a **counter function**.
This returned function should initially return `n`, and then return one more than the previous value every time it's called (`n`, `n+1`, `n+2`, ...).

---

## 📥 Input

* An integer `n` (initial value of the counter)
* An array of operations (always containing the string `"call"`)

---

## 📤 Output

* An array of integers representing the return values of each `call` to the counter function.

---

## 💡 Examples

### Example 1

```js
Input:
n = 10
calls = ["call", "call", "call"]

Output:
[10, 11, 12]

Explanation:
const counter = createCounter(10);
counter(); // 10
counter(); // 11
counter(); // 12
```

---

### Example 2

```js
Input:
n = -2
calls = ["call", "call", "call", "call", "call"]

Output:
[-2, -1, 0, 1, 2]

Explanation:
const counter = createCounter(-2);
counter(); // -2
counter(); // -1
counter(); // 0
counter(); // 1
counter(); // 2
```

---

## 🔧 Constraints

* `-1000 <= n <= 1000`
* `0 <= calls.length <= 1000`
* `calls[i] === "call"`

---

## ✅ Solution (JavaScript)

```js
var createCounter = function(n) {
  return function() {
    return n++;
  };
};
```

---

## 📌 Notes

* This problem helps you understand **closures** and **stateful functions** in JavaScript.
* Useful in building custom counters, timers, or generators.


