Here’s a clean and professional **README format** for the `Counter II` problem — suitable for GitHub or documentation:

---

# Counter II

**Difficulty**: Easy
**Category**: JavaScript / Closures / Functions

---

## 📘 Description

Implement a function `createCounter` that accepts an integer `init`. It should return an object with the following three methods:

* `increment()` → Increases the current value by 1 and returns it.
* `decrement()` → Decreases the current value by 1 and returns it.
* `reset()` → Resets the current value to the initial `init` value and returns it.

---

## 🧪 Examples

### Example 1

```js
Input:
const counter = createCounter(5);
counter.increment(); // 6
counter.reset();     // 5
counter.decrement(); // 4

Output: [6, 5, 4]
```

### Example 2

```js
Input:
const counter = createCounter(0);
counter.increment(); // 1
counter.increment(); // 2
counter.decrement(); // 1
counter.reset();     // 0
counter.reset();     // 0

Output: [1, 2, 1, 0, 0]
```

---

## ✅ Constraints

* `-1000 <= init <= 1000`
* `0 <= calls.length <= 1000`
* Each call is one of: `"increment"`, `"decrement"`, `"reset"`

---

## 💡 Hint

Use closures to maintain the internal state across function calls.

---

## 🧠 Solution (JavaScript)

```js
var createCounter = function(init) {
    let current = init;

    return {
        increment: () => ++current,
        decrement: () => --current,
        reset: () => current = init
    };
};
```
