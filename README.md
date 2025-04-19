# 📘 JavaScript Cheatbook

Welcome to the **JavaScript Cheatbook** – a concise, curated reference for JavaScript concepts, key questions, and detailed answers. This repository aims to serve as a handy guide for beginners, intermediates, and even experienced developers looking for quick refreshers.

Whether you're preparing for interviews, brushing up your basics, or learning JavaScript from scratch, this cheatbook will help you understand the **core concepts**, backed with clear explanations and real-world analogies.

---

## 🔹 1. JavaScript – An Overview

JavaScript is a **lightweight**, **object-based**, and **interpreted** scripting language. It is the backbone of web interactivity and is supported by all modern web browsers.

### 🧠 Key Features

- **Lightweight** – Minimal memory usage, concise syntax, and fast execution.
- **Object-Based** – Supports most OOP concepts *except* full polymorphism and classical inheritance.
- **Interpreted** – JavaScript is not compiled traditionally but interpreted line-by-line by the browser.
- **Dynamic & Weakly Typed** – Variables are not bound to a specific data type and can change at runtime.
- **Case Sensitive** – Variable and function names are case-sensitive.

### 🧩 Object-Based Language

- Supports OOP concepts like encapsulation and abstraction.
- You can create objects and classes.
- Traditional inheritance and polymorphism (like in Java or C++) are not fully supported.

---

## 📜 Scripting Language

- No need for compilation.
- Interpreted at runtime – line by line.
- Ideal for fast development and rapid iteration.
- Easier to learn and quicker to code than structured languages like C or C++.

---

## 💡 What is a Compiled Language?

- Source code is translated into machine code using a **compiler**.
- Code is parsed, optimized, and translated **before** execution.
- Offers faster and more efficient execution.
- Examples: **C**, **C++**, **Java**.

---

## ⚙️ JavaScript is Interpreted

- The browser’s **JavaScript engine** interprets the code at runtime.
- Slower than compiled languages, but modern browsers use **JIT (Just-In-Time) compilation** to close the performance gap.

### 🔍 Real-World Analogy

> Suppose you have a Persian recipe and you only understand English.  
> You have two options:  
> 1. Translate the entire recipe beforehand (Compiled).  
> 2. Have someone translate it for you line by line while you cook (Interpreted).

- In the second case, if the recipe changes midway, the interpreter can adapt on the fly – **just like JavaScript.**

---

## 🚀 JIT – Just-In-Time Compilation

- A hybrid of compilation and interpretation.
- Code is compiled *during execution* rather than before.

### 🔧 Two Traditional Approaches:
1. **AOT (Ahead-of-Time) Compilation**
2. **Interpretation**

---

## 🧠 How JIT Works in Browsers

Modern JavaScript engines (like **V8**, used in Chrome, Opera, Node.js) use JIT.

### ⚙️ V8 Components

- **Ignition**:  
  - Compiles JS source code into **bytecode**, not machine code.  
  - Fast and compact, improving efficiency.

- **TurboFan**:  
  - Analyzes and optimizes bytecode in the background.  
  - Generates highly optimized machine code.  
  - Replaces bytecode with machine code without interrupting execution.

---

## 📊 JavaScript Data Types

JavaScript is **dynamically typed** and **weakly typed**, meaning:

- Variables don’t require explicit type declaration.
- Data types can change at runtime.

### 🔸 Primitive Data Types

- `String`
- `Number`
- `BigInt`
- `Boolean`
- `Null`
- `Undefined`
- `Symbol`

🧾 *Primitive data types store a single value.*

---

### 🔹 Non-Primitive Data Types

- `Object` (includes arrays, functions, etc.)

🧾 *Non-Primitive types are used to store multiple values or key-value pairs.*

---

### 🟡 Special Data Types

#### `undefined`
Represents a variable that has been declared but not assigned a value.

```js
let data;
console.log(data); // undefined


### 🔁 Arrow Functions in JavaScript

- Introduced in **ES6**
- Provide a **shorter syntax** for writing functions
- Handle the `this` keyword **lexically**, so there's **no need to bind `this`**
- `this` refers to the context in which the function was defined (not called)
- ✅ Use cases:
  - Implicit returns
  - Avoiding `this` binding issues

---

#### ❌ Using Regular Function (Incorrect `this` context)
```js
function Counter() {
  this.count = 0;

  setInterval(function () {
    this.count++; // 'this' refers to the global object (e.g., window)
    console.log(this.count);
  }, 1000);
}

const counter = new Counter();
```

#### ✅ Using Arrow Function (Correct `this` context)
```js
function Counter() {
  this.count = 0;

  setInterval(() => {
    this.count++; // 'this' correctly refers to the Counter instance
    console.log(this.count);
  }, 1000);
}

const counter = new Counter();
```


