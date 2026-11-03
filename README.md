# NYC Airbnb Listings Under the 30-Night Rule

COMP 418 Data Mining, Bridgewater State University, Fall 2026, Lensi Gondaliya

**Question:** What kinds of Airbnb listings exist in New York City under Local Law 18, which allows stays under 30 nights only when the host is present?

## Data
`listings.csv.gz` is the Inside Airbnb New York City detailed listings file, scraped 14–15 September 2026 (29,918 listings, 90 columns). Source: [insideairbnb.com](http://insideairbnb.com/get-the-data/), licensed CC BY 4.0.

## Notebooks (run in this order)
1. `airbnb_eda.ipynb`: data dictionary, quality checks, cleaning, and preprocessing. Saves `listings_clean.csv`.
2. `eda.ipynb`: exploratory analysis of price by borough and room type, license status, host size, and a map.
3. `prepared_dataset.ipynb`: final features for mining. Saves `prepared_clustering.csv` and `prepared_transactions.csv`.

## Planned mining methods
- Clustering (k-means)
- Association rules (Apriori)
- Anomaly detection (Isolation Forest)

## Environment
Python 3 (Anaconda) with pandas, numpy, and matplotlib.
