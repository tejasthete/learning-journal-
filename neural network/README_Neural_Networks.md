# 🧠 Neural Networks: Daily Learning Log

I'm starting neural networks from the very basics: one neuron first, then layers, then full networks. This folder holds the notebooks and a short note for every day I work on it.

> **Status:** 🚧 Just started (Day 1: 2026-11-23). Notebooks are work in progress and I list known issues openly below.

---

## 🎯 Goal

Understand how neural networks actually work, from a single perceptron up to training a multi-layer network, by coding each idea myself on small examples before using bigger libraries.

**Tools:** Python, NumPy, scikit-learn, Matplotlib (TensorFlow / PyTorch later)

---

## 🗺️ Roadmap

- [x] Perceptron (AND, OR, XOR)
- [x] Activation functions (step, sigmoid, tanh, ReLU, softmax)
- [ ] Multi-layer perceptron and solving XOR
- [ ] Forward propagation
- [ ] Loss functions
- [ ] Gradient descent
- [ ] Backpropagation
- [ ] Overfitting and regularisation in networks
- [ ] First network in TensorFlow / PyTorch

*The roadmap is tentative and will change as I learn.*

---

## 📅 Daily Log

| Day | Date | Topic | Notebook | Key takeaway |
|---|---|---|---|---|
| 1 | 2026-11-23 | Perceptron and activation functions | [Perceptron_Logic_Gates](./Perceptron_Logic_Gates.ipynb), [Perceptron_and_Activation_Functions](./Perceptron_and_Activation_Functions.ipynb) | A single perceptron solves AND and OR (100%) but only reaches 50% on XOR, because XOR is not linearly separable |
| 2 | *YYYY-MM-DD* | *Topic* | *link* | *takeaway* |

> Add one row per day at the bottom.

---

## 📘 Day 1 Summary

**Experiment:** trained scikit-learn's `Perceptron` on the AND, OR and XOR gates and plotted five activation functions.

| Gate | Accuracy | Why |
|---|---|---|
| AND | 100% | Linearly separable |
| OR | 100% | Linearly separable |
| XOR | 50% | One straight line cannot separate the classes |

**What I learned**
- A perceptron is a weighted sum plus a bias, passed through a step function, so it can only draw one straight decision boundary.
- XOR failing is the reason hidden layers and non-linear activations exist.
- Activation functions shape a neuron's output: step gives hard 0/1, sigmoid squashes to (0, 1), tanh to (-1, 1), ReLU zeroes out negatives, and softmax turns scores into probabilities.

**Known issues in the Day 1 notebooks (to fix)**
- Sigmoid is written as `1/1+np.exp(-z)` and should be `1/(1+np.exp(-z))`.
- ReLU uses `np.maximum(-1, z)` and should be `np.maximum(0, z)`.
- Accuracy for the OR and XOR models in the logic-gates notebook was scored against the AND model's predictions, so the printed numbers there are wrong. The correct values are 100% and 50%.

---

## 🧾 Daily Entry Template

```markdown
## Day N | YYYY-MM-DD | Topic

**What I did**
- 

**Results**
- 

**Key learnings**
- 

**Mistakes caught and fixed**
- 

**Next:** 
```

---

## 📁 Structure

```
neural-networks/
├── README.md
├── Perceptron_Logic_Gates.ipynb
├── Perceptron_and_Activation_Functions.ipynb
└── ...   # one notebook per topic
```

---

Feedback and corrections are welcome.
