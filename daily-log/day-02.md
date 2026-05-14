# Day 2 — Python Foundations for JARVIS

**Date:** 2026-05-14  
**Start:** 18:56  
**End:** 20:47  
**Duration:** 1h 51m  
**Status:** ✅ Complete

---

## 🎯 Goal
Build the Python foundation needed to construct a conversational AI agent (JARVIS). Cover all syntax and data structures used in the upcoming Groq API integration.

---

## 📚 Topics Covered

### 1. Variables & Data Types
- `str`, `int`, `float`, `bool`
- `type()` for inspecting types
- Variable naming rules

### 2. Strings & f-strings
- String creation and concatenation
- f-strings: `f"Hello {name}"`
- Methods: `.upper()`, `.lower()`, `.strip()`

### 3. Lists
- Creation: `[]`
- Indexing (positive & negative)
- `.append()` to add items
- `len()` for size

### 4. Dictionaries
- Key-value pairs: `{"key": "value"}`
- Access via `dict["key"]`
- Add / update / delete keys
- **List of dictionaries** (the JARVIS message format)

### 5. Conditionals
- `if`, `elif`, `else`
- Comparison operators: `==`, `!=`, `<`, `>`, `<=`, `>=`
- Logical operators: `and`, `or`, `not`
- `=` vs `==` distinction

### 6. Loops
- `for item in collection:`
- `range(n)`
- `while condition:`
- `break` keyword
- Manual index tracking with `while`

### Bonus Tools Picked Up
- `input()` — user input
- `int()` — string-to-int conversion
- `del` — remove keys/variables

---

## 🧪 Hands-On Exercises Completed
- [x] Variable type experiments
- [x] f-string formatting
- [x] List creation + append
- [x] List of dictionaries (chat history structure)
- [x] If/elif/else mood responder
- [x] Mini JARVIS chat loop (`while True` + `break`)
- [x] Number guessing game
- [x] While loop with list filtering (`value <= 4`)

---

## 🐛 Bugs Hit & Lessons Learned

| Bug | Root Cause | Lesson |
|-----|-----------|--------|
| `AttributeError: 'list' object attribute 'append' is read-only` | Used `list.append = (...)` instead of `list.append(...)` | `=` is assignment, `()` calls a method |
| `TypeError: 'str' object is not callable` on `input()` | Earlier cell shadowed the built-in `input` with a string variable | Never name variables after Python built-ins |

---

## 💡 Key Insight
The JARVIS architecture skeleton uses **every** concept from today:

```python
messages = []                                                # list
messages.append({"role": "system", "content": "..."})        # dict in list
while True:                                                  # loop
    user_input = input("You: ").strip().lower()             # input + strings
    if user_input == "bye":                                  # conditional
        break
    messages.append({"role": "user", "content": user_input})
