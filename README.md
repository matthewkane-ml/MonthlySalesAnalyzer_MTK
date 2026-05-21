# Monthly Sales Analyzer

> A pure-Python sales analysis tool built on a 20-day, 3-product dataset — implementing eight analytical functions from scratch using only loops, conditionals, and data structures.

---

## Problem

Before reaching for pandas or NumPy, a data analyst needs to understand how to extract insights directly from raw Python structures. This project builds a full sales analysis pipeline using only native Python — no external libraries — to answer the kinds of questions any business stakeholder would ask: which product leads, which day peaked, how many days crossed a target threshold.

## Dataset

A list of 20 dictionaries, each representing one day of sales for three products:

```python
{"day": 1, "product_a": 202, "product_b": 142, "product_c": 164}
```

- 20 days × 3 products (A, B, C)
- No external file — data is defined directly in `monthly_sales_analyzer.py`

## Functions Implemented

| Function | Description |
|---|---|
| `total_sales_by_product(data, key)` | Sum all daily sales for a given product |
| `average_daily_sales(data, key)` | Mean daily sales for a given product |
| `best_selling_day(data)` | Day number with highest combined sales across all products |
| `days_above_threshold(data, key, threshold)` | Count days where a product's sales exceeded a threshold |
| `top_product(data)` | Which of A/B/C had the highest total sales over the period |
| `worst_selling_day(data)` *(bonus)* | Day with the lowest combined sales |
| `show_top_three(data)` *(bonus)* | Top 3 days ranked by total sales |
| `get_range(data, key)` *(bonus)* | Max − min spread for a given product |

## Results

Across the 20-day period:

- **Top product:** Product C — consistently the highest daily volume, totaling ~5,300 units vs ~3,750 for A and ~2,435 for B
- **Best selling day:** Day 12 (combined total ~690 units: 287 + 64 + 339)
- **Product C days above 300:** 8 out of 20 days

The three bonus functions were also implemented. `show_top_three` works by calling `best_selling_day` iteratively and popping the found day from a copy of the list — a clean reuse of existing logic without duplicating code.

## Tech Stack

`Python` · native data structures only (lists, dicts, loops, conditionals)

## Run It Locally

```bash
git clone https://github.com/matthewkane-ml/MonthlySalesAnalyzer_MTK.git
cd MonthlySalesAnalyzer_MTK
python monthly_sales_analyzer.py
```

No dependencies to install — pure Python.

## What I'd Do Next

- Refactor the loops to use Python built-ins (`sum()`, `max()`, `min()`, list comprehensions) now that the manual logic is understood — the natural next step after this exercise
- Load the data from a CSV file so the analyzer works on real month-end sales exports
- Add a visualization layer with Matplotlib to plot daily totals and product trends over time

---

**Author:** Matthew Kane — [LinkedIn](https://www.linkedin.com/in/thomas-k-392094410/) · [GitHub portfolio](https://github.com/matthewkane-ml)
