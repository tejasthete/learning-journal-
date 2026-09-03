# Hotel Bookings – Data Analysis Practice 📊

This repo is part of my day-to-day learning journal where I practice data cleaning, data transformation, and exploratory data analysis (EDA) using Python and pandas. I'm using the Hotel Bookings dataset to work through a set of self-made questions, step by step, to strengthen my data analytics fundamentals.

## Why this repo?
I'm building my skills in data science/analytics one dataset at a time. Instead of just watching tutorials, I'm solving real questions on real data and tracking my progress here — mistakes, learnings, and all.

## Dataset
`hotel_bookings.csv` — 119,390 rows, 32 columns of hotel booking data (City Hotel + Resort Hotel), including lead time, cancellations, ADR, market segment, guest details, and more.

## Files
```
├── hotel_bookings.csv              # Dataset
├── Hotelbooking_Questions.txt      # Questions I'm solving
├── Solved_answers.ipynb            # My answers, question by question + EDA charts
└── README.md
```

## What I'm practicing

**Data Cleaning**
- Checking shape, columns, data types
- Finding & handling missing values
- Spotting duplicates and invalid values (zero ADR, zero adults, etc.)
- Basic summary stats (lead time, ADR)
- Exploring unique categories (meal, market segment, deposit type, etc.)

**Data Transformation**
- Creating new columns like `Total_Nights` and `Total_Guest`

**EDA**
- Comparing hotels by bookings & cancellation rate
- Finding booking trends by month
- Seeing how lead time relates to cancellations
- Which market segment brings in the most bookings
- Visualizing everything with matplotlib/seaborn:
  - Total bookings by hotel (count plot)
  - % of bookings cancelled (pie chart)
  - Cancelled vs not cancelled by hotel (stacked bar)
  - Cancellations by market segment (bar chart)
  - Average ADR by hotel (column chart)
  - Monthly booking demand (line chart)
  - Average ADR by month (line chart)
  - Bookings by customer type (donut chart)
  - Lead time vs cancellation (strip/scatter chart)

## Tools
Python, pandas, numpy, matplotlib, seaborn

## Progress Log
- [x] Data cleaning questions (Q1–Q37)
- [x] Data transformation
- [x] EDA questions + charts

(Next up: maybe dig into feature engineering or try the same questions in SQL.)

## Notes to self
Jotting down anything I learn or find interesting while solving these — patterns in the data, pandas tricks, gotchas, etc.

- `groupby()` + `.mean()` is doing a lot of heavy lifting for cancellation rate questions
- Learned `unstack()` to reshape grouped data for stacked bar charts
- Donut chart is just a pie chart with `wedgeprops = dict(width=0.5)`

---

This is a learning-in-public repo — not polished, just consistent practice. 🚀
