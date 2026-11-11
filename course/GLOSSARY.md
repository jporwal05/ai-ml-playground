# Glossary

Every term taught in the course, in plain English, with its analogy.

| Term | Plain-English meaning | Analogy | Lesson |
|---|---|---|---|
| Machine learning (ML) | Getting a computer to find a rule from examples, instead of a human writing the rule. | A child learning "dog" from examples, not a rulebook. | [01](../concepts/01-what-is-ml/README.md) |
| Data / example | The examples we learn from: each one is a question paired with its correct answer (e.g. size → price). | The dogs (and non-dogs) you point at for the child. | [01](../concepts/01-what-is-ml/README.md) |
| Model | The rule the computer builds; something that takes a question and returns a prediction. | A machine with knobs. | [01](../concepts/01-what-is-ml/README.md) |
| Parameter | A number inside the model that can be adjusted, such as `m` (tilt) and `b` (shift) of a line. | A knob on the machine. | [01](../concepts/01-what-is-ml/README.md) |
| Training (learning) | Adjusting the parameters, step by step, until predictions match the real answers. | Turning the knobs until the machine's output is right. | [01](../concepts/01-what-is-ml/README.md) |
| Prediction | The model's answer for a question, especially one it never saw in the data. | The child naming a dog breed they've never met. | [01](../concepts/01-what-is-ml/README.md) |
| Function | A recipe that turns an input into an output, the same way every time. In ML, the model is a function. | A taxi meter: km in, fare out. | [02](../concepts/02-model-is-a-function/README.md) |
| Input (x) | The number you give the model: the question (km, pizza size). Changes with every use. | The distance of each ride. | [02](../concepts/02-model-is-a-function/README.md) |
| Output (y) | The number the model gives back: its prediction (fare, price). | The fare shown on the meter. | [02](../concepts/02-model-is-a-function/README.md) |
| Slope / weight (m or w) | The tilt knob: how much y changes when x goes up by 1. Called "weight" in neural networks. | The taxi's per-km rate. | [02](../concepts/02-model-is-a-function/README.md) |
| Intercept / bias (b) | The shift knob: the value of y when x = 0, where the line crosses the vertical axis. Called "bias" in neural networks. | The taxi's base fare. | [02](../concepts/02-model-is-a-function/README.md) |
| Linear / non-linear | Linear: the data follows a straight line. Non-linear: it curves (e.g. rises then falls), so no straight line fits. | Taxi fares (linear) vs temperature over a day (non-linear). | [02](../concepts/02-model-is-a-function/README.md) |
| Loss | One number that measures how wrong a model is across all examples. Lower is better; 0 is perfect. Training = making it smaller. | A golf score: one number for the whole round, lower wins. | [03](../concepts/03-loss/README.md) |
| Error / miss (residual) | Real answer minus prediction: y − ŷ. Positive = model too low, negative = model too high. | The gap between where the ball landed and the hole. | [03](../concepts/03-loss/README.md) |
| Mean Squared Error (MSE) | Square each miss, then average them. Squaring stops misses cancelling and punishes big misses most. | A speeding fine that grows fast: small mistakes cost a little, big ones cost a lot. | [03](../concepts/03-loss/README.md) |
| ŷ (y-hat) | The model's prediction. The hat means "a guess"; plain y is the real answer. | The meter's estimate vs the actual fare. | [03](../concepts/03-loss/README.md) |
| Loss curve | A plot of the loss for many values of a knob. For MSE with a line it's a U-shaped valley; the best knob value is at the bottom. | A valley you're standing in, blindfolded. | [03](../concepts/03-loss/README.md) |
| Slope | How much the output changes per step to the right: rise ÷ run. Negative = going down, positive = going up, 0 = flat. | The tilt you feel under your foot on a hillside. | [04](../concepts/04-derivatives/README.md) |
| Derivative (dL/dm) | The slope of the loss at one exact spot, for an infinitely tiny slide of the knob. Its sign says which way to turn the knob; its size says how far from the bottom. | Feeling the ground's tilt while standing still, blindfolded. | [04](../concepts/04-derivatives/README.md) |
| Tangent line | A straight line that touches a curve at one spot with the curve's exact tilt there. Height anywhere = spot height + spot slope × (m − spot). | A rigid skateboard resting on a bowl. | [04](../concepts/04-derivatives/README.md) |
| Slide size h | The tiny amount you nudge a knob to measure a slope. Too big gives a wrong reading on steep curves; shrink it until the answer stops changing. | How far you slide your foot to feel the ground. | [04](../concepts/04-derivatives/README.md) |
