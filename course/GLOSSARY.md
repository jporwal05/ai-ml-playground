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
