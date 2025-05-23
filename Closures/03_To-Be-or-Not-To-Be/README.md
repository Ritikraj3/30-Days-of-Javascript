Here’s a **classic and professional README file** for the **"To Be Or Not To Be"** problem, formatted in Markdown style for developer portfolios or GitHub projects:

---

# ✅ To Be Or Not To Be

### ✔️ Solved | 🟢 Easy | 💼 Common in Developer Tooling Scenarios

---

## 🧩 Problem Statement

Implement a utility function `expect` to assist developers in testing their code.
The `expect` function should accept any value and return an object with two assertion methods:

* `toBe(val)` — returns `true` if the given value is **strictly equal** (`===`) to the original value, otherwise throws an error: `"Not Equal"`.
* `notToBe(val)` — returns `true` if the given value is **not strictly equal** (`!==`) to the original value, otherwise throws an error: `"Equal"`.

---

## 🧪 Function Signature

```javascript
function expect(val: any): {
  toBe: (expected: any) => boolean,
  notToBe: (unexpected: any) => boolean
}
```

---

## 📥 Input

* A single value of any type to be passed to `expect(val)`.
* An assertion method call: `toBe(val)` or `notToBe(val)`.

---

## 📤 Output

* Returns `true` if the assertion passes.
* Throws an error with a message `"Not Equal"` or `"Equal"` if it fails.

---

## 💡 Examples

### Example 1

```js
const result = () => expect(5).toBe(5);
// Output: { "value": true }
```

### Example 2

```js
const result = () => expect(5).toBe(null);
// Output: { "error": "Not Equal" }
```

### Example 3

```js
const result = () => expect(5).notToBe(null);
// Output: { "value": true }
```

---

## 🔧 Constraints

* All types are supported as inputs (`number`, `string`, `null`, `object`, etc.).
* Comparison should use **strict equality (`===`)** and **strict inequality (`!==`)**.
* Only `toBe()` and `notToBe()` methods should be implemented.

---

## ✅ Sample Solution (JavaScript)

```js
var expect = function(val) {
  return {
    toBe: function(expected) {
      if (val === expected) return true;
      else throw new Error("Not Equal");
    },
    notToBe: function(unexpected) {
      if (val !== unexpected) return true;
      else throw new Error("Equal");
    }
  };
};
```

---

## 🛠️ Use Cases

* Lightweight custom test utility
* Understanding closures and method chaining
* Demonstrates handling assertion logic manually

---

## 📚 Related Concepts

* Closures
* Object return patterns
* JavaScript testing patterns (Jest-like syntax)

---

> ✨ This utility mimics the style of testing libraries like [Jest](https://jestjs.io/), and is a great starting point for understanding how test assertions are built from scratch.
