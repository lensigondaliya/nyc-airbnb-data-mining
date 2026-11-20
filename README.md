# NYC Airbnb Listings Under the 30-Night Rule

COMP 418 Data Mining, Bridgewater State University, Fall 2026, Lensi Gondaliya

**Question:** What kinds of Airbnb listings exist in New York City under Local Law 18, which allows stays under 30 nights only when the host is present?

## Data
`listings.csv.gz` is the Inside Airbnb New York City detailed listings file, scraped 14–15 September 2026 (29,918 listings, 90 columns). Source: [insideairbnb.com](http://insideairbnb.com/get-the-data/), licensed CC BY 4.0.

## Notebooks (run in this order)
1. `airbnb_eda.ipynb`: data dictionary, quality checks, cleaning, and preprocessing. Saves `listings_clean.csv`.
2. `eda.ipynb`: exploratory analysis of price by borough and room type, license status, host size, and a map.
3. `prepared_dataset.ipynb`: final features for mining. Saves `prepared_clustering.csv` and `prepared_transactions.csv`.
4. `Mining.ipynb`: k-means clustering (k = 6), association rules (Apriori), and anomaly detection (Isolation Forest). Saves `mining_rules.csv` and the `mining_*.png` figures.
5. `Sensitivity.ipynb`: compares k = 3 with k = 6. Saves `sensitivity_k3_vs_k6.png`.

## Main findings
- 80.7% of listings require 30+ nights; most sit exactly at the 30-night line.
- Six listing groups, including popular short stays, hotel rooms, and monthly whole homes.
- Short stays outside Manhattan are mostly registered; Manhattan short stays are mostly exempt hotels.
- Isolation Forest flagged 388 unusual listings (2%): large, expensive, rarely booked.
- With k = 3, the short-stay and monthly groups stay the same, but hotels and big operators disappear, so k = 6 was kept.

These are patterns in the data, not proof that any host broke the law.

## Environment
Python 3 (Anaconda) with pandas, numpy, matplotlib, scikit-learn, and mlxtend 0.25.0.
