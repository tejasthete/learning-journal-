# Machine Learning

Hands-on notebooks from my structured ML learning track. This folder starts with the basics and grows toward more advanced topics, one notebook at a time. I learn in public, so everything here is a work in progress. Some notebooks use small toy datasets on purpose, so I can see exactly what each concept does before applying it to real data.

**Stack:** Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn

## What I've covered so far

| Topic | What I practiced |
|---|---|
| **Linear Regression** | Fitting lines, reading slope and intercept, perfect vs. noisy data, a negative-slope example (car price depreciation), train/test split, error metrics (MAE, MSE, RMSE) |
| **Polynomial Regression** | `PolynomialFeatures` + `LinearRegression`, underfitting vs. good fit vs. overfitting, a degree-9 polynomial experiment to see overfitting on test data |
| **Encoding categorical data** | Label Encoder (one number per category) and One-Hot Encoder (one binary column per category) |
| **Logistic Regression** | Binary classification, `predict` vs. `predict_proba`, threshold-based prediction, confusion matrix, accuracy / precision / recall / F1 on two toy datasets (one cleanly separable, one not) |
| **Decision Trees** | `DecisionTreeClassifier` on two toy datasets (loan approval, weather/play prediction), Gini impurity vs. entropy as split criteria, `max_depth` and `criterion` tuning, visualizing trees with `plot_tree`, encoding categorical features (Label vs. One-Hot) for tree input |
| **Decision Trees 2** | Built a second tree (Age + FB time → ad click). All leaves hit gini = 0.0 — perfect fit on 4 rows, same overfitting pattern as the earlier degree-9 polynomial. Also hit an UndefinedMetricWarning: 5-row dataset + test_size=0.2 left only 1 test sample, so precision/recall/F1 came back 0.0 despite 1.0 accuracy.|
## Key lessons so far

- **Scale after splitting.** Fit `StandardScaler` on the training data only, then use `transform` on the test data. Fitting on the test set leaks information.
- **Stratify small splits.** An unstratified split can leave a class out of the test set, which makes precision, recall and F1 undefined. `stratify=y` prevents it.
- **Tiny test sets prove little.** A perfect score on two test samples is not evidence that a model works.
- **Overfitting is visible only on unseen data.** A high-degree polynomial can fit the training set closely and still fail on the test set.
- **Shapes matter.** `X` is a 2D matrix, `y` is a 1D vector, and `.predict()` always needs 2D input.
- **Trees need numeric input.** Unlike linear/logistic regression, a raw categorical column throws a hard error on `.fit()` — encoding isn't optional.
- **Encoding choice changes column count, not just values.** One-Hot expands a single categorical column into N binary columns, which silently changes how many features the model expects at prediction time — every downstream `.predict()` call has to match that shape exactly.

## How I work

- One notebook per topic, growing from basics to advanced.
- Self-generated questions and experiments, not copied tutorials.
- Bugs I hit along the way are part of the record. Stale variable names, mismatched inputs and out-of-order cells all taught me something.
- Daily entries in the learning journal, with dated commits.

## Status and next steps

Work in progress. Planned next: regularization, gradient descent, Random Forests (building on the Decision Tree foundation), and re-running the classification experiments with stratified splits to compare metrics before and after.
