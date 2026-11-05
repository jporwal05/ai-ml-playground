# Progress

## Setup
- [x] Install uv + Python 3.12
- [x] Project environment (numpy, matplotlib, Jupyter)
- [x] VS Code Python + Jupyter extensions

## Concepts learned
| # | Lesson | Notes |
|---|---|---|
| 01 | [What is ML?](concepts/01-what-is-ml/README.md) | Quick check: 4/4. Fit the pizza line by hand (m = 1.029, b = 1.089, 16-inch → $17.55). Chose knobs by "getting the line close to all the points" — an intuition for loss, without a number yet. |
| 02 | [A model is just a function](concepts/02-model-is-a-function/README.md) | Quick check: 3/3 (phone plan). Explained m = 0 (flat line, base fare only) and why lines cross x = 0 at b. Solved battery 0% = 12.5 h by algebra. Spotted unprompted that curved data is *non-linear* and a line can't fit it. Slip: linspace point count. |

## Weak spots to watch
- Math gets overwhelming when it jumps from simple ideas to notation. Rule: picture → tiny numbers by hand → code → symbols last, with at most one new symbol per step.
- Matrices.
- Small coding habits: reuse variables (`m`, `b`) instead of retyping numbers; log attempts; count points in `linspace`.
- Sometimes leaves "why" questions unanswered: prompt for the why before moving on.

## Next up
Lesson 03 — Loss: one number for "how wrong".
