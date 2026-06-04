# 📅 Day 3 — Building JARVIS's Core

## 🎯 Goal
Build a working AI chatbot with personality and memory using the Groq API.

## ✅ What I Did Today
- 🔑 Loaded API key securely via environment variables
- 📞 Created the Groq client and made my FIRST API call
- 🔍 Extracted the clean reply from the messy response object
- 🎭 Gave JARVIS a personality using a system prompt
- 🧠 Added memory with a chat loop (JARVIS remembers context!)

## 🧩 Concepts Learned
- `import` vs `from...import`
- Environment variables for secrets
- Objects & dot-diving: `response.choices[0].message.content`
- List of dicts → the `messages` structure
- The 3 roles: system / user / assistant
- `while True:` loop + `break`
- `.append()` to grow memory
- f-strings for output

## 💡 Key Insight
Each API call is STATELESS — sending the full `messages` list every time IS the memory.

## 🪞 Honest Reflection
Realized I was copy-pasting too much. Called it out.
Switching to "I guide, you build" from Day 4 — writing code myself.
Starting Python practice (Exercism/PyBites) in parallel.

## 🗺️ Next Up (Day 4)
- Rebuild the chat loop BY WRITING IT MYSELF
- Possible upgrade: timestamps / command shortcuts / streaming

## ⏱️ Status
Day 3 ✅ Complete — JARVIS talks, has personality, and remembers.
