
````markdown
#  Control Flow Statements Cheat Sheet

A **quick, professional reference** to the four key control flow keywords in programming: **break, continue, return, throw**.  
```
---

## 🛑 1️⃣ BREAK
- **Scope:** Loops (`for`, `while`) & `switch`  
- **Purpose:** Exit the loop or switch **immediately**  
- **Example:**
```python
for i in range(5):
    if i == 3:
        break
    print(i)
# Output: 0 1 2
````
```
> Stops execution of the loop entirely when a condition is met.
```
---
```
## ⏭️ 2️⃣ CONTINUE

* **Scope:** Loops only
* **Purpose:** Skip the **current iteration** and move to the next
* **Example:**
```
```python
for i in range(5):
    if i == 3:
        continue
    print(i)
# Output: 0 1 2 4
```
```
> Useful when you want to ignore certain cases without stopping the whole loop.
```
---
```
## 🔙 3️⃣ RETURN

* **Scope:** Functions
* **Purpose:** Exit a function and optionally **return a value**
* **Example:**
```
```python
def square(x):
    return x * x

print(square(4))
# Output: 16
```
```
> Any code after `return` inside the function **won’t run**.
```
---
```
## ⚠️ 4️⃣ THROW / RAISE

* **Scope:** Anywhere in code (commonly in functions)
* **Purpose:** Raise an **exception/error** and jump to an error handler
* **Example:**
```
```python
def divide(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero")
    return a / b

try:
    divide(5, 0)
except ValueError as e:
    print("Error:", e)
# Output: Error: Cannot divide by zero
```
```
> Immediately stops normal execution and moves to error handling.
```
---
```
## 📊 Quick Comparison

| Keyword    | Scope         | Effect                           |
| ---------- | ------------- | -------------------------------- |
| `break`    | Loops, switch | Exit loop/switch immediately     |
| `continue` | Loops         | Skip current iteration           |
| `return`   | Functions     | Exit function, return value      |
| `throw`    | Anywhere      | Raise exception, jump to handler |
```
---
```
## 💡 Pro Tip

* **`break` & `continue`** → control **loop flow**
* **`return`** → control **function flow**
* **`throw`** → control **error flow**

> Keep this cheat sheet handy for writing clean, readable code!

```

