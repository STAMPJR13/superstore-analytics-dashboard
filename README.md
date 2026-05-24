# 🛒 Superstore Profitability Dashboard

A profitability diagnostic on the public **Sample Superstore** dataset (9,994 order lines · 5,009 orders · 2014–2017), built as a **2-page Power BI dashboard** and replicated **chart-for-chart in Python** (pandas + matplotlib) so the analysis is fully reproducible.

> **The question:** Superstore is profitable overall — so where is it *quietly losing money*?

---

## 🔑 Headline finding

| Metric | Value |
|---|---|
| Revenue | **$2.30M** |
| Total Profit | **$286K** |
| Margin | **12.47%** |
| Avg Discount | 15.62% |
| **Loss rate (line items)** | **18.72%** |
| Orders | 5,009 |

---

## 📊 The dashboard

### Page 1 — Sale Dashboard *(descriptive: "what does the business look like?")*
- **KPI cards** — revenue, profit, margin, discount, loss %, orders
- **Sales & Profit by Year** — sales +52%, profit +89% (2014→2017), but loss rate stays flat at ~18.7% → growth sits *on top of* a stable leak
- **Sales by Year & Month** — a repeating **Q4 peak / February trough** every year
- **By Segment** — Consumer biggest by sales ($1.16M) but worst margin (11.6%); Home Office smallest yet best (14.0%)
- **By Region** — Central runs **7.9%** margin, roughly **half** of the West (14.9%)
- **By Category** — Technology 17.4% & Office Supplies 17.0%, but **Furniture just 2.5%** (first red flag)

### Page 2 — Profitability & Discount Analysis *(diagnostic: "where & why is profit destroyed?")*
- **Average Profit by Discount Bucket** — positive ≤20%, negative in every bucket above (low of –$299 at 41–50%)
- **Loss-Rate by Discount Bucket** — the key chart: loss rate jumps **14% → 91.6%** crossing 20%, and hits **100% above 40%**
- **Sales by Sub-Category** — top sellers: Phones, Chairs, Storage, **Tables**, Binders
- **Profit by Sub-Category** — **Tables is the worst at –$17.7K** despite being a top-4 seller; **Copiers the best at +$55K** on protected pricing

---

## 💡 Recommendations (each tied to a chart)

1. **Cap discounts at 20%** — evidence: loss rate goes 14% → 91.6% crossing the threshold.
2. **Re-cost or discontinue Tables** — top-4 seller but the single biggest profit leak (–$17.7K).
3. **Protect Copiers' pricing** — most profitable line (+$55K); no volume discounts.
4. **Pre-stock Q4 inventory** — the seasonal peak repeats every year.


