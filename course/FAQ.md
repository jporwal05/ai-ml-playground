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

## Lesson 02 — A model is just a function

**Why does `b` decide where the line crosses the vertical axis?**
At x = 0, the tilt part is `m × 0 = 0`, so only `b` is left: y = b. In taxi terms, a 0 km ride costs just the base fare.

**Why does `np.linspace(0, 12, 12)` give strange decimals?**
The third number is *how many points*, spread evenly from start to end. 0 to 12 in whole steps needs 13 points (12 gaps need 13 fence posts). Use `np.linspace(0, 12, 13)` or `np.arange(0, 13)`.

**The battery model predicts −20% at 15 hours. Is the model broken?**
No. It just follows its formula. A model knows nothing about the real world beyond its function and knobs. Always sanity-check predictions, especially outside the range of your data.
