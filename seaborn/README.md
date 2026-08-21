# Seaborn Line Plot — Daily Journal

Practice notebook covering line plots with Seaborn, built on top of Matplotlib.

## What's inside

- Basic line plot with plain Matplotlib (`plt.plot()`) for comparison
- Creating a DataFrame from a dictionary and plotting it with `sns.lineplot()`
- Using `hue` and `style` to group lines by category (e.g. Gender)
- Customizing markers, marker size, line width, and line style
- Hiding the legend with `legend=False`
- Loading a real dataset (`tipss.csv`) and plotting `total_bill` vs `tip`
- Grouping by `sex` and `smoker`, with custom marker shapes and the `"muted"` color palette

## Dataset

`tipss.csv` — the classic Seaborn tips dataset (total bill, tip, sex, smoker, day, time, size).

## Requirements

```
pandas
matplotlib
seaborn
```

## Notes

- `sns.lineplot()` needs `plt.show()` (from Matplotlib) to actually render — Seaborn has no `show()` of its own.
- `hue` groups by color, `style` groups by line/marker style — usually pick one, not both, unless you want extra emphasis.
