# Restaurant Sales Analysis

A business-oriented data analysis of the sales of a **real, family-owned
restaurant** (Frontera Comalapa, Chiapas), covering **January 2025 – October 2026**.

The goal was a practical "business health diagnosis": understand how revenue,
customer traffic and average ticket evolved through a period of major change —
the restaurant relocated, raised prices, and lost a nearby street market that
used to drive foot traffic — and turn that into clear, actionable conclusions
for the owner.

The analysis grew from a single notebook into six focused ones, each covering
one business question end to end: takeout vs. dine-in, general sales trends,
product performance, customer affluence (party size, inferred), tips as a
service-quality signal, and weather's effect on buying behavior.

## Key findings (Jan–Sep, 2025 vs. 2026)

- **Food revenue 2025: ~$1.86M MXN.**
- Tickets fell **−7.0%** year over year, while the average ticket rose **+12.4%**
  — more moderate than the owner's own preliminary read (10–20% fewer tickets,
  up to +35% average ticket), but the same direction: fewer, higher-value sales.
- **Dine-in vs. takeout diverge:** the dine-in ticket jumped to **$317** (+20%),
  while takeout stayed flat at **$238**. Dine-in also pulled ahead on revenue
  share (59%→61%) despite a slightly smaller share of tickets.
- **Tipping rate (dine-in) dropped from 6.6% to 5.0%** of the ticket over the
  same window — a real signal worth watching for service quality after the move
  to a bigger space.
- **Rain measurably lowers the average ticket** (~12% lower, controlling for
  hour/month/year) — partial support for the "people duck in just for a drink"
  theory, though tickets don't fall all the way to a single-drink price. Heat
  alone shows a much weaker effect.
- Solo diners are the single largest party-size group (~41% of dine-in sales,
  inferred from repeated dishes per sale), ahead of pairs (~35%) and groups
  (~19%); family-tagged sales peak on Sunday, consistent with the location next
  to the church and park.
- Rent represents **~14% of sales** in the new, larger location (from the
  executive report's Jan–Jun 2026 cut).
- **Verdict:** the business absorbed the relocation and the loss of its
  neighboring market while keeping revenue growing through price, not volume.
  Health is good; the next challenge is filling the larger new location.

## Approach

1. **Data consolidation** — unify yearly sales workbooks into a clean dataset.
2. **Cleaning & feature engineering** — normalize dates, products and channels;
   derive monthly aggregates, ticket counts and average ticket.
3. **Sales analysis** — year-over-year revenue, traffic and ticket comparison,
   split by channel (dine-in vs. takeout), product and customer affluence.
4. **Growth analysis** — month-by-month trends framed against the business
   events (relocation, price change, loss of the nearby market).
5. **Communication** — an executive report and a business-diagnosis
   presentation aimed at a non-technical owner.

## Deliverables

- [`reports/restaurant_sales_executive_report.pdf`](reports/restaurant_sales_executive_report.pdf)
- [`reports/business_health_diagnosis.pdf`](reports/business_health_diagnosis.pdf)
- `notebooks/`:
  1. [`01_mostrador_vs_local.ipynb`](notebooks/01_mostrador_vs_local.ipynb) — takeout vs. dine-in, by hour/day, plus aggregated frequent-customer behavior.
  2. [`02_ventas_generales.ipynb`](notebooks/02_ventas_generales.ipynb) — tickets and average ticket by month/hour/day, hour×day heatmap.
  3. [`03_productos.ipynb`](notebooks/03_productos.ipynb) — best- and worst-selling products and categories.
  4. [`04_afluencia_clientes.ipynb`](notebooks/04_afluencia_clientes.ipynb) — party size (solo/pair/group/family), inferred from repeated dishes per sale.
  5. [`05_propinas.ipynb`](notebooks/05_propinas.ipynb) — tip rate as a service-quality proxy, by hour/day.
  6. [`06_clima_ventas.ipynb`](notebooks/06_clima_ventas.ipynb) — weather vs. ticket volume and average ticket.

## Repository structure

```
notebooks/   # six sales analysis notebooks, one per question (see Deliverables)
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
