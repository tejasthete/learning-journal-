# Scatter Plot with Seaborn

A short notebook demonstrating how to create scatter plots using `seaborn` and `matplotlib`, covering point coloring, sizing, and styling by category.

## Contents

- **Study Hours vs Marks** — a simple scatter plot from a manually created DataFrame, using `hue` and `size` to encode the `Marks` column.
- **Tips Dataset** — a scatter plot of `tip` vs `total_bill` using seaborn's built-in `tips` dataset, with points colored by `sex` and styled by `day` using different markers.

## Requirements

```
pandas
matplotlib
seaborn
```

Install with:

```bash
pip install pandas matplotlib seaborn
```

## Usage

Open the notebook and run all cells:

```bash
jupyter notebook Scatter_plot.ipynb
```

## Key Seaborn Parameters Covered

| Parameter | Description |
|---|---|
| `x`, `y` | Columns to plot on each axis |
| `data` | DataFrame containing `x` and `y` |
| `hue` | Colors points based on a column's values |
| `size` | Scales point size based on a column's values |
| `sizes` | `(min, max)` range for point sizes |
| `style` | Varies marker style based on a column's values |
| `markers` | Custom marker shapes to use |
| `alpha` | Point transparency |
