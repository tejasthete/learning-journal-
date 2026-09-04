# 📚 Learning Journal
Documenting my daily learning journey in Python, data visualization, and data analysis — one topic, one commit at a time.

## 🎯 Purpose
This repo is where I track what I learn every day. Instead of scattered notes, everything lives here — searchable, organized, and visible as a timeline of progress.

## 🗂️ Topics Covered
- **Matplotlib** — data visualization (line charts, bar charts, pie charts, scatter plots, subplots, fill_between)
- **Seaborn** — statistical data visualization built on Matplotlib (line plots, bar plots, count plots, pair plots, histograms, KDE plots, box plots, hue/style grouping, markers, color palettes)
- **Applied EDA** — putting Matplotlib/Seaborn to work on a real dataset (Hotel Bookings): data cleaning, transformation, and chart-driven analysis

## 📅 Progress Log
| Date | Topic | What I Learned |
|------|-------|-----------------|
| 2026-08-20 | Matplotlib | `subplot()` — displaying multiple charts in one figure |
| 2026-08-21 | Seaborn | `lineplot()` basics — hue & style for grouping, custom markers, marker size, line width/style, hiding the legend, loading real datasets (tips) with pandas |
| 2026-08-24 | Seaborn | `scatterplot()` — hue & size to encode a numeric column, sizes range for point scaling, style + custom markers for categorical grouping, alpha for transparency, plotting real datasets (tips) |
| 2026-08-25 | Seaborn | `barplot()` — grouping with hue, dodge for separating bars, order & hue_order for custom positioning, palette styling, estimator (mean/sum) and capsize for error bars, width control |
| 2026-08-25 | Seaborn | `countplot()` — visualizing counts of a single categorical column, hue for sub-grouping, palette and width customization |
| 2026-08-25 | Seaborn | `pairplot()` — visualizing pairwise relationships between numerical variables, off-diagonal scatter plots & diagonal KDE/histograms, hue for categorical grouping, vars/x_vars/y_vars for selecting specific columns |
| 2026-08-27 | Seaborn | `histplot()` — binning a numeric column, hue for sub-grouping, multiple = "stack" vs "layer" for combining groups, element & kde overlay, palette styling; `kdeplot()` — smooth density curves, bw_adjust for smoothing, clip to restrict range, fill vs outline, multiple = "layer", hue_order for custom legend order; `boxplot()` — comparing distributions across categories, orient for horizontal/vertical boxes, hue for sub-grouping, color & saturation styling |
| 2026-09-02 | Pandas / EDA | Worked through the Hotel Bookings dataset (119,390 rows) — data cleaning (missing values, duplicates, invalid entries) and data transformation (adding `Total_Nights`, `Total_Guest` columns) as self-made practice questions |
| 2026-09-03 | Matplotlib & Seaborn | Applied EDA to Hotel Bookings dataset with 9 charts: count plot (bookings by hotel), pie chart (% cancelled), stacked column (cancellations by hotel), bar chart (cancellations by market segment), column chart (avg ADR by hotel), line charts (booking demand & ADR by month), donut chart (bookings by customer type), scatter/strip plot (lead time vs cancellation) |
|2026-09-04	|Matplotlib	plt.subplots |— combined 6 individual charts into one Hotel Booking Dashboard (hotel bookings, cancellation ratio, monthly trend, market segment, waiting list, reservation status) using fig.suptitle(), per-axis ax[row,col].set_title(), and plt.tight_layout()


## 🛠️ Tools & Tech
- Python
- Jupyter Notebook
- Matplotlib
- Seaborn
- Pandas

## 📌 How This Repo Works
- Each topic gets its own folder as I add more subjects (Pandas, SQL, etc.)
- Notebooks are updated as I learn more on that topic
- Commit messages describe what was learned that day

## ⭐ Feel free to follow along as this grows!
