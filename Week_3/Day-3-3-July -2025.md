###  Asynchronous JavaScript Course (Async/Await, Promises, Callbacks)

 - Why we use asynchronous And what does it means ??
 
 - It allow you to break down bigger project into smaller tasks.
 - And then using any of these 3 methods either , callbacks, promises, or async awai
 - 
## JSON (javascript object Notation )

 **- Data Representation Format
 - commonly used for APIS and configs
 - Lightweight and easy to Read/Write
 - Integrated easily with most languages**
 
  **

## JSON Types

**
**1.Strings
 2.. Numbers
     3. Booleans
     4. Arrays
     5. Null
     6.Objects*

---

## ⏳ 1. Asynchronous JavaScript

### 🔹 What is "async"?

- **Async** code runs **without blocking** the main thread.
- Useful for handling **time-consuming tasks** (API calls, file loading, etc.).

### 🔹 Common async patterns:
- **Callbacks** – Old style (can get messy – callback hell)
- **Promises** – More manageable
- **`async/await`** – Modern and clean syntax built on top of promises

---

## 🔁 2. Promises

- A **Promise** represents a value that may be available **now, later, or never**.
- Has three states:
  - `pending`
  - `fulfilled`
  - `rejected`

---

## ✅ 3. `async` and `await`

- `async` makes a function return a Promise.
- `await` pauses the code **inside an async function** until the Promise resolves.

### 🧠 Why It Matters:
- Allows writing **asynchronous code in a synchronous style**
- Cleaner, readable, and less error-prone

---

## 📤 4. JavaScript Modules

### 🔸 Why Modules?

- Organize code into **reusable, isolated files**
- Avoid naming conflicts
- Enable **code sharing** between files or projects

### 🔹 `export`

- Used to **make variables, functions, or classes public** from a module.

### 🔹 `import`

- Used to **bring exported code into another file**.

### 🧠 Things to Remember:

| Feature       | Use                          |
|---------------|-------------------------------|
| `export`      | Share code from a module      |
| `import`      | Use shared code in another file |
| File type     | Must be `.js` or `.mjs` with `"type": "module"` in `package.json` |
| Must be top-level | Can't be inside functions or conditions |

---

## 🌐 5. JSON (JavaScript Object Notation)

### 🔹 What is JSON?

- A **lightweight data format** used to store and exchange data.
- Looks like a JS object but is in **string format**.

### 🔹 Why JSON Matters:

- Used for data transfer between frontend and backend
- Common in APIs, config files, databases

### 🔧 Key Methods:

| Method            | Purpose                            |
|-------------------|-------------------------------------|
| `JSON.stringify()` | Convert JS object → JSON string    |
| `JSON.parse()`     | Convert JSON string → JS object    |

---

## 🌍 6. Fetching JSON Data (Asynchronous)

- Often used with `fetch()` to **get data from APIs**
- Can be combined with `async/await` for cleaner code

---

## 📌 Summary – What to Remember

| Concept        | Key Idea                                      |
|----------------|-----------------------------------------------|
| `async/await`  | Clean way to handle asynchronous operations   |
| `Promise`      | Handles success or failure of async actions   |
| `export/import` | Enables modular and maintainable code        |
| `JSON`         | Standard data format for web communication    |
| `stringify()`  | Converts object → string for storage/sending  |
| `parse()`      | Converts string → object for JS usage         |

---

> 💡 Tip: Use modules + async code together to build clean, scalable, and maintainable JavaScript apps.

