# FAQ

Questions learners asked during lessons, with answers.

## Setup

**Where do I create a notebook file like `test.ipynb`?**
In the top folder of the project (next to `pyproject.toml`). In VS Code's Explorer, hover over the project name, click **New File**, and type the name. Then use **Select Kernel → Python Environments → `.venv`** so the notebook uses the project's libraries.

## Lesson 01 — What is ML?

**Does every problem need ML?**
No. If you can write the exact rule (km → miles, tax on a bill), just write it. Use ML when the pattern is easy to *see* but impossible to *write down* (handwriting, song recommendations).

**My knob values are very precise (like m = 1.029). Are they the "right" answer?**
There's no single right line when finding it by eye. Many lines fit almost equally well. To say one line is *better* than another, we need one number that measures "how wrong" a line is. That number is the **loss**, in Lesson 03.
