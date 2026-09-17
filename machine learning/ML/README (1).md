# Linear Regression — End-to-End Pipeline (Practice Notebook)

A minimal, from-scratch walkthrough of the full supervised learning workflow using Scikit-learn's `LinearRegression`: build data → encode categoricals → split → train → predict → evaluate.

This is a **learning notebook, not a portfolio project.** The dataset is synthetic and tiny (7 rows). The point was to get the mechanics of the pipeline into muscle memory, and to see what the evaluation metrics actually look like when they come out the other end.

---

## Results

| Metric | Value |
|---|---|
| MAE | ~7.8e-06 |
| MSE | ~6.3e-11 |
| RMSE | ~8.0e-06 |
| R² | ~0.99999999999 |

**These numbers mean nothing, and that's the most useful thing in the repo.**

`Price` in this dataset is exactly `House_Size / 200 + 5` — a perfectly deterministic linear function of a single feature. The model recovered that relationship to floating-point precision because there was nothing else to recover. There's no noise, no unexplained variance, and only two rows in the test set.

The takeaway I'm carrying forward: **an R² this close to 1 on real data is a bug signal, not a win.** It usually means leakage, a target accidentally included in the features, or a feature that's a proxy for the label. Learning to be suspicious of a good score is worth more than learning to produce one.

---

## What the notebook covers

1. **Dataset construction** — a pandas DataFrame with `House_Size`, `Total_Resource`, `Age`, `Location` (categorical), and `Price` as the target.
2. **Categorical encoding** — `pd.get_dummies()` on `Location` with `dtype=int` to produce clean 0/1 indicator columns.
3. **Feature/target separation** — `X = df.drop("Price", axis=1)`, `y = df["Price"]`.
4. **Train/test split** — `train_test_split` with `test_size=0.2`, `random_state=42` (5 train / 2 test).
5. **Model fitting** — `LinearRegression().fit(X_train, y_train)`.
6. **Prediction and residual inspection** — actual vs. predicted printed side by side, then the raw differences.
7. **Evaluation** — MAE, MSE, RMSE, and R² from `sklearn.metrics`.

## Stack

`Python` · `pandas` · `scikit-learn`

---

## Known issues (work in progress)

Keeping these visible rather than quietly fixing them, since tracking my own mistakes is part of the point of this repo.

- **R² is computed incorrectly.** The line reads `r2_score(y_test, prediction) ** 0.5` — the square root is left over from confusing R² with RMSE. The `** 0.5` needs to go.
- **Variable name mismatch.** Predictions are stored as `predication`, but the metrics cell references `prediction`. That cell only executed because a stale `prediction` object was still in the kernel. A clean *Restart & Run All* would raise `NameError`.
- **Column name mismatch.** The dict key is `"Total_Resource"`, but the saved cell outputs all show `Total_Resources` — the stored outputs came from an earlier version of the cell. Needs a full re-run before the notebook is trustworthy.
- **Test set is two rows.** No metric computed on two samples is meaningful. `cross_val_score` or LOOCV would be the honest alternative at this size.
- **Cosmetic** — a stray trailing comma in the actual-vs-predicted print loop, and `res = model.fit(...)` is assigned but only ever prints `LinearRegression()`.

## Next steps

- Fix the bugs above and commit a clean *Restart & Run All*.
- Re-run the identical pipeline on a real dataset (California Housing) so the metrics have something to say.
- Add residual plots and an actual-vs-predicted scatter — evaluating a regression by reading four numbers isn't enough.
- Compare against Ridge and Lasso once there's real noise and multicollinearity to regularize against.

---

Part of my ongoing [ML learning journey](https://github.com/) — documenting the work in public, including the parts that aren't finished yet.
