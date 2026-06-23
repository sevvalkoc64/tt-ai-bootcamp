# 🤖 TT AI Bootcamp

> A hands-on, two-week journey from "what even *is* AI?" all the way to building agents — taught through live coding, lots of interruptions, and plenty of **I/We/You** practice.

Welcome! This repository holds the notebooks for an intensive AI bootcamp. We start with the absolute fundamentals of Python and build up, day by day, toward modern Generative AI, RAGs, and agents. Bring your curiosity — and your keyboard.

---

## 🗺️ Curriculum

### Week 1 — Foundations
- **Introduction to AI** — the big picture and where everything fits
- **Introduction to Python** — the language we'll live in
- **Introduction to SQL** (DuckDB)
- **ML Fundamentals**
- **Deep Learning**
- **GenAI & LLMs**

### Week 2 — Going Further
- **Advanced Machine Learning**
- **Embeddings & RAGs**
- **MCP, Agents & AgentOps**

### 🧠 What "AI" actually covers
This bootcamp is grounded in the classic map of the field (à la [*Artificial Intelligence: A Modern Approach*](https://aima.cs.berkeley.edu/)):

- Rule-based systems
- Search algorithms — DFS, BFS, CSP, Beam Search, Dynamic Programming
- Logic & Probabilistic Reasoning
- Machine Learning — Supervised / Unsupervised, Reinforcement Learning, Deep Learning, Transformers and beyond
- Communication, Perceiving & Acting — NLP, Computer Vision, Robotics & Control Theory

---

## 📜 House Rules
- 🙋 **Interrupt, ask, and talk!!!** — this is the most important rule.
- 🎥 Keep your screens on at all times during online sessions.
- ☕ A short break every **45 minutes**.
- 👣 We learn by **I do → We do → You do**.
- 🏆 Everything builds toward your **Capstone** project.

---

## 📅 Day 1 — Python from Zero to Classes

Day 1 is a fast, practical tour of Python — the toolkit you'll reuse every single day afterward. We move from arithmetic to designing clean, object-oriented systems, with a recurring eye on how these basics show up in **real AI/NLP problems**.

Work through the notebooks in order:

| # | Notebook | What you'll learn |
|---|----------|-------------------|
| 01 | [`010_Basics.ipynb`](010_Basics.ipynb) | Numbers & arithmetic (`/` vs `//` vs `%`), and string quoting |
| 02 | [`020_Boolean.ipynb`](020_Boolean.ipynb) | `True`/`False`/`None`, comparisons, chained comparisons, `==` vs `is` |
| 03 | [`030_Conditionals.ipynb`](030_Conditionals.ipynb) | `if`/`elif`/`else` and the ternary expression |
| 04 | [`040_Looping.ipynb`](040_Looping.ipynb) | `for` loops, `range`, `enumerate`, and `zip(..., strict=True)` |
| 05 | [`050_Comprehension.ipynb`](050_Comprehension.ipynb) | List comprehensions — turning loops into one expressive line |
| 06 | [`060_String.ipynb`](060_String.ipynb) | f-strings, string methods, slicing, and a first taste of tokenization |
| 07 | [`070_Dictionaries.ipynb`](070_Dictionaries.ipynb) | Dicts, `.get()`, dict comprehensions — and **why sparse beats dense** for NLP matrices |
| 08 | [`080_Func.ipynb`](080_Func.ipynb) | Functions, type hints, and passing functions as arguments (`Callable`) |
| 09 | [`085_Func.ipynb`](085_Func.ipynb) | Building real ML metrics (`MAE`, `RMSE`, `Jaccard`) and composing them |
| 10 | [`090_Class.ipynb`](090_Class.ipynb) | `@dataclass`, `frozen`/`slots`, methods, and a tiny `RunApp` |
| 11 | [`100_SampleCode.ipynb`](100_SampleCode.ipynb) | Refactoring a "god class" into clean, single-responsibility components |

### 🎯 Highlights & "aha!" moments

- **From loop to comprehension.** Splitting even and odd numbers with an explicit loop, then collapsing it into `[i for i in range(101) if i % 2 == 0]`.
- **Tokenization without libraries.** Lowercasing, slicing, and filtering stop words straight off `"The quick brown fox..."` — the raw mechanics behind every NLP pipeline.
- **Sparse vs. dense, with the math.** A dense document × term matrix would cost ~**364 TB**; the sparse equivalent is ~**7.5 GB**. This is *why* dictionaries (and `.get(key, 0)`) matter at scale.
- **Functions are values.** A single `do_calculation(op, a, b)` dispatches to `add`, `sub`, `mult`, or `div` — the seed of pluggable, composable design.
- **Real metrics, composed.** Implement `MAE`, `RMSE`, and `Jaccard` from scratch, register them in a dict, then build a weighted `super_metric` on top.
- **Designing with dataclasses.** Model a `Run` (frozen + slotted) with `speed()` and `pace()`, then wrap it in a `RunApp` that finds your best and longest runs.
- **The refactoring challenge.** Take a 100-line `SuperSystemManager` god class — auth, inventory, pricing, discounts, payment, logging, and email all in one method — and progressively break it apart using dataclasses, `Protocol`s, and separation of concerns. (Yes, the rough drafts have bugs on purpose — spotting them is part of the lesson!)

> 💡 By the end of Day 1 you'll be comfortable reading and writing idiomatic Python — and you'll have seen, first-hand, how plain language features connect to machine learning and NLP.

---

Happy hacking — and remember: **interrupt, ask, and talk!** 🎉
