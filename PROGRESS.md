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
| 03 | [Loss](concepts/03-loss/README.md) | Quick check: 3/3 (cancelling, MSE = 2.5, D beats C). Wrote `mse` cleanly; beat own Lesson 01 score by nudging (0.0775 → 0.0763); found loss curve is U-shaped with best m = 1.03. Blindfold answer: "feel inclined downwards", a ready intuition for slope. Slip: passed `prices` as x in the bonus. |
| 04 | [Derivatives as direction](concepts/04-derivatives/README.md) | Quick check: 3/3 (slopes −1.9 and +2.1, gentle slope = near the bottom). Wrote `slope(f, m, h)` cleanly; saw h → 0 approach −4. Pizza loss first scored only one pizza, then fixed to all 5; discovered h = 0.01 gives the wrong sign at m = 1.03. Tangent lines were the hardest part: needed the skateboard explanation and, finally, the code. |

## Weak spots to watch
- Math gets overwhelming when it jumps from simple ideas to notation. Rule: picture → tiny numbers by hand → code → symbols last, with at most one new symbol per step.
- Matrices.
- Small coding habits: reuse variables (`m`, `b`) instead of retyping numbers; log attempts; count points in `linspace`.
- Tangent lines (Lesson 04): kept using each point's height/slope instead of the spot's. The skateboard + "rise = slope × run" explanation was written up for the course; revisit when tangents return (gradient descent, backprop).
- Input vs output mix-ups (passed `prices` as x in Lesson 03): ask "what is x here?" when reviewing.
- Sometimes leaves "why" questions unanswered or vague ("walk down the curve"): push for an exact, computer-followable answer.

## Next up
Lesson 05 — Gradient descent: walking downhill step by step.
