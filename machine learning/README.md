# Linear Regression — Basics to Advanced

An evolving notebook tracking my journey through Linear Regression — starting from first-principles intuition with `scikit-learn` and building up toward more advanced regression techniques over time.

This is a living document — new sections get added as I progress, rather than a one-off exercise.

## Progress Roadmap

- [x] Simple Linear Regression (1 feature) — perfect vs. imperfect linear data
- [ ] Multiple Linear Regression (many features)
- [ ] Feature scaling & normalization
- [ ] Train/test split and evaluation metrics (MAE, MSE, RMSE, R²)
- [ ] Polynomial Regression
- [ ] Regularization: Ridge & Lasso
- [ ] Handling multicollinearity (VIF)
- [ ] Gradient Descent from scratch
- [ ] Assumption checks (linearity, homoscedasticity, normality of residuals)
- [ ] Applying to a real dataset end-to-end (e.g. California House Price)

*(Checklist will be updated as each topic is covered.)*

## Section 1: Simple Linear Regression (Basics)

### 1. Perfect Linear Data
```python
X = [[1000], [2000], [3000], [4000], [5000]]
y = [10, 20, 30, 40, 50]
```
The data follows `y = 0.01x` exactly. The model recovers:
- **Slope (m):** `0.01`
- **Intercept (c):** `~0` (tiny floating-point noise, e.g. `-7.1e-15`)
- **Prediction at x=10000:** `100.0` ✅ (matches `0.01 × 10000`)

**Key learning:** floating-point arithmetic in Python/NumPy can't always represent decimals exactly, so an intercept that's mathematically `0` may print as a near-zero number like `1e-15`. This is expected — not a bug.

### 2. Real-World (Imperfect) Linear Data
```python
a = [[4], [6], [8], [10]]
b = [12, 24, 36, 72]
```
This data is **not** perfectly linear — the jump from `(8, 36)` to `(10, 72)` breaks the constant rate of change seen in the first three points. The model finds the **best-fit line** using least squares:
- **Slope (m):** `9.6`
- **Intercept (c):** `-31.2`
- **Prediction at x=12:** `84.0` (verified: `9.6 × 12 - 31.2 = 84`)

**Key learning:** `LinearRegression` doesn't require perfectly linear data — it minimizes the total squared error across all points, producing the closest possible straight-line approximation. This is what real datasets look like, versus clean textbook examples.

## Visualizations
- Scatter plot of the perfect linear data (Example 1)
- Scatter plot of actual data points overlaid with the fitted regression line (Example 2) — visually shows how the line balances error across points that don't sit exactly on it

## Concepts Covered
- `model.fit(X, y)` — training a linear regression model
- `model.coef_` and `model.intercept_` — extracting slope (m) and intercept (c)
- `model.predict()` — always requires 2D input, e.g. `[[10000]]`
- Least squares line fitting on noisy/imperfect data
- Floating-point precision quirks in numerical output

## Tools Used
`scikit-learn`, `matplotlib`, `numpy`

## Notes
This notebook is part of my ongoing ML learning journal. Each new concept (multiple regression, regularization, polynomial fits, etc.) will be appended as a new section with its own code, output, and takeaway — so this file doubles as both a notebook and a running reference as I move from basics to advanced regression.
