### 
# 📘 JavaScript Crash Course – Week 3 Notes

> JavaScript fundamentals including variables, data types, comparisons, conditionals, and a touch of OOP.

---

## 🔤 JavaScript Variables

### `var`, `let`, and `const`

| Keyword | Scope       | Reassignable | Hoisted | Best Practice |
|---------|-------------|--------------|---------|----------------|
| `var`   | Function    | ✅ Yes        | ✅ Yes  | ❌ Avoid        |
| `let`   | Block       | ✅ Yes        | ❌ No   | ✅ Preferred     |
| `const` | Block       | ❌ No         | ❌ No   | ✅ For constants |

```js
var a = 10;
let b = 20;
const c = 30;

