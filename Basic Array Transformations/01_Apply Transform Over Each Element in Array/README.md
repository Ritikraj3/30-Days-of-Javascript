

# 🔁 Apply Transform Over Each Element in Array

### 🟢 Easy | 💼 Common in Interviews | 🚫 No `Array.map` Allowed

---

## 🧩 Problem Statement

You are given an integer array `arr` and a **mapping function** `fn`.
Return a new array with the transformation applied to each element such that:

```js
result[i] = fn(arr[i], i)
```

> ⚠️ **Do not use the built-in `Array.map` method** to solve this problem.

---

## 📥 Input

* `arr`: an array of integers.
* `fn`: a function that takes in two arguments — the element value and its index.

---

## 📤 Output

* A new array where each element is the result of applying `fn(val, index)` on the original array.

---

## 💡 Examples

### Example 1

```js
Input:
arr = [1, 2, 3]
fn = function plusOne(n) { return n + 1; }

Output:
[2, 3, 4]

Explanation:
Each element is incremented by 1.
```

---

### Example 2

```js
Input:
arr = [1, 2, 3]
fn = function plusIndex(n, i) { return n + i; }

Output:
[1, 3, 5]

Explanation:
Each element is increased by its index.
```

---

### Example 3

```js
Input:
arr = [10, 20, 30]
fn = function constant() { return 42; }

Output:
[42, 42, 42]

Explanation:
The function always returns 42, regardless of input.
```

---

## 🔧 Constraints

* `0 <= arr.length <= 1000`
* `-10⁹ <= arr[i] <= 10⁹`
* `fn` returns an integer

---

## ✅ Sample Solution (JavaScript)

```js
var map = function(arr, fn) {
  const result = [];
  for (let i = 0; i < arr.length; i++) {
    result.push(fn(arr[i], i));
  }
  return result;
};
```

---

## 📚 Key Concepts

* Higher-order functions
* Array iteration
* Function parameters (value and index)

---

## 🚫 Why No `Array.map`?

This problem tests your understanding of **manual array transformation**, not just reliance on built-in helpers. It’s a great practice for:

* Custom data transformation
* Working in environments without modern array methods
* Building your own utilities
