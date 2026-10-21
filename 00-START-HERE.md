# Start Here

New to coding, or new to Python? Read this once (about 15 minutes) before Episode 01.
You don't need to memorize anything here. Come back whenever you need it.

---

## 1. What you need

- A **Google account**, to run notebooks in Google Colab (free, in your browser, no install).
- A free **GitHub account**, only for Core and Stretch missions. Starter missions don't need it.

## 2. Your first notebook in Colab

1. In any episode folder, click the **Open in Colab** badge.
2. A notebook is a list of **cells**. Text cells explain; code cells run Python.
3. **Run a cell:** click the ▶ button on its left, or press **Ctrl+Enter** (Cmd+Enter on Mac).
   **Shift+Enter** runs the cell and moves to the next one.
4. Run cells **from top to bottom**. Order matters: a cell can only use what earlier cells created.
5. **Save your own copy:** `File → Save a copy in Drive`. The original stays clean for everyone.
6. **Before you call it done:** `Runtime → Restart session and run all`.
   If everything still works from a clean start, your notebook is truly working. This is the habit Episode 01 is about.

> Stuck in a weird state? `Runtime → Disconnect and delete runtime`, then run all cells again from the top.

## 3. Already know another language? Python in 60 seconds

| In many languages | In Python |
|---|---|
| `{ }` braces for blocks | **Indentation** (4 spaces) defines blocks, and it's required |
| `;` at line ends | No semicolons |
| `true / false / null` | `True / False / None` (capitalized) |
| `&& / \|\| / !` | `and / or / not` |
| `int x = 5;` | `x = 5` (no type declaration needed) |
| `arr.length` | `len(arr)` |
| String formatting | f-strings: `f"Hello {name}"` |
| `// comment` | `# comment` |

Indexing starts at 0, like in most languages.

## 4. The 10 Python ideas you'll see first

```python
name = "Ada"                            # a variable: a name for a value
score = 9.5                             # numbers: int (9) and float (9.5)
words = ["learn", "build", "break"]     # a list: ordered items
counts = {"learn": 1, "build": 2}       # a dict: key -> value lookups

def greet(person):                      # a function: reusable steps
    return f"Hi {person}"

for word in words:                      # a loop: repeat for each item
    print(word)

if score > 9:                           # a condition: choose a path
    print("great")

import math                             # import: use code someone else wrote
print(math.sqrt(16))                    # prints 4.0
```

Every notebook also has short **Python pit-stops**: collapsed cells you can open when a line confuses you.

## 5. How to read an error

Errors are information, not failure. In Python, **read the last line first**. It names the error type and the reason. Then read upward to find the line that caused it.

For example, if you defined `total` but typed `totl`, the last line says something like:

```text
NameError: name 'totl' is not defined
```

Depending on where you run it, Python may also add a hint like *Did you mean: 'total'?*

## 6. Learning with AI assistants (the rules we use)

1. **Predict first.** Before asking, write what you think the answer is.
2. **Ask it to explain, not just to write.** "Why does this line work?" teaches you more than "fix my code".
3. **Verify by running.** AI assistants can confidently invent things. Episode 03 shows how to catch that.
4. **Never paste passwords, API keys, or private data** into a chat or a notebook.

## 7. Next steps

- Watch **Episode 00** and post your Starter comment.
- Fork this repo (top-right **Fork** button = your own copy) to track your progress in the README checklist.
- Ready for more? [LOCAL-SETUP.md](LOCAL-SETUP.md) shows how to run everything on your own computer. It's optional.
