# Restaurant Sales Analysis

A business-oriented data analysis of the sales of a **real, family-owned
restaurant** (Frontera Comalapa, Chiapas), covering **January 2025 – June 2026**.

The goal was a practical "business health diagnosis": understand how revenue,
customer traffic and average ticket evolved through a period of major change —
the restaurant relocated, raised prices, and lost a nearby street market that
used to drive foot traffic — and turn that into clear, actionable conclusions
for the owner.

## Key findings

- **Food revenue 2025: ~$1.86M MXN.**
- Revenue held up: **+1.4%** vs. the same period in 2025...
- ...while customer traffic fell: **−4.8% tickets**.
- The business sustained revenue by raising the **average ticket (+6.5%)** —
  i.e. charging more to fewer customers.
- Rent represents **~14% of sales** in the new, larger location.
- **Verdict:** the business absorbed the relocation and the loss of its
  neighboring market while keeping revenue stable. Health is good; the next
  challenge is making the larger new location more profitable.

## Approach

1. **Data consolidation** — unify yearly sales workbooks into a clean dataset.
2. **Cleaning & feature engineering** — normalize dates, products and channels;
   derive monthly aggregates, ticket counts and average ticket.
3. **Sales analysis** — year-over-year revenue, traffic and ticket comparison.
4. **Growth analysis** — month-by-month trends framed against the business
   events (relocation, price change, loss of the nearby market).
5. **Communication** — an executive report and a business-diagnosis
   presentation aimed at a non-technical owner.

## Deliverables

- [`reports/restaurant_sales_executive_report.pdf`](reports/restaurant_sales_executive_report.pdf)
- [`reports/business_health_diagnosis.pdf`](reports/business_health_diagnosis.pdf)
- [`notebooks/restaurant_sales_analysis.ipynb`](notebooks/restaurant_sales_analysis.ipynb)

## Repository structure

```
notebooks/   # sales analysis notebook
reports/     # executive report + business-health diagnosis (PDF)
data/        # data is private — see data/README.md
```

## Data privacy

The raw records belong to a private business and are **not published** here.
The notebook documents the full methodology, and the reports share aggregated,
non-identifying results. See [`data/README.md`](data/README.md).

## Tech stack

Python · Pandas · NumPy · Matplotlib

## License

Released under the [MIT License](LICENSE).
