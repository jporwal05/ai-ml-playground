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

## Lesson 03 — Loss

**Why can't we just add up the misses?**
Positive and negative misses cancel. A flat line that's $4 too high on one pizza and $4 too low on another sums to 0, which falsely looks "perfect".

**Why square instead of just dropping the minus sign?**
Both stop the cancelling. Squaring also punishes big misses much more (a miss of 4 costs 16, not 4), so the model focuses on its worst mistakes. It also makes a smooth U-shaped loss curve, which matters for finding "downhill" in the next lessons.

**How do I find "downhill" on the loss curve without seeing the whole curve?**
Feel the tilt where you stand: if the ground slopes down to the right, increase the knob. That tilt is the slope (derivative), covered in Lesson 04.

## Lesson 04 — Derivatives as direction

**My tangent line bends and follows the curve. What's wrong?**
You're computing the height and slope at *every point* instead of *once at the spot*. Picture a rigid skateboard resting on the bowl: measure the spot's height and slope once, then walk along the board using rise = slope × run. Board height at any m = spot height + spot slope × (m − spot). At m = 1 (height 4, slope −4), the ends are (0.2, 7.2) and (1.8, 0.8). See the lesson's skateboard section.

**Why isn't the board's height the same as the curve's height away from the spot?**
The board is straight and the curve bends. At m = 1.8 the board is at 0.8, but the curve is at 1.44. They only match at the spot, which is what "touching" means.

**With h = 0.01, the slope at the bottom had the wrong sign. Why?**
"Tiny" depends on the curve. On a steep-walled valley, a 0.01 slide already climbs partway up the far wall. Shrink `h` until the answer stops changing.

**Why not just try every knob value, like in Lesson 03?**
It explodes: 101 values per knob means 101 × 101 = 10,201 tries for two knobs, and an impossible number for millions. The slope gives the direction with two loss calculations per knob.
