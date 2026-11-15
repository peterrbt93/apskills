---
name: python-function-descriptions
description: Write or improve docstrings that describe Python functions without changing their implementation.
---

# Python Function Descriptions

When asked to describe Python functions, make changes only to function docstrings.

- Add or revise docstrings for functions and methods; do not modify executable code, comments, type annotations, or module and class docstrings.
- Describe behavior evident from the implementation. Do not invent guarantees, side effects, exceptions, or performance characteristics.
- State the function's purpose and, when useful, explain meaningful arguments, return values, raised exceptions, and side effects.
- Keep descriptions concise and use the documentation style already present in the file. If no style is established, use a short summary followed by Google-style `Args`, `Returns`, and `Raises` sections only where applicable.
- Preserve existing behavior exactly. If a function's behavior is unclear, describe only what can be verified from its implementation.
- Do not add descriptions to functions unless requested, and do not make unrelated cleanup changes.
- Make docstrings in Danish