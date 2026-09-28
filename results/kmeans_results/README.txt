Exploratory K-means on MP-EVData daily electrical load curves.
Stations: A1-A6, A9, A10; A7/A8 counts excluded.
Coverage: available complete days in 2024; A10 has 96 days.
Input: 2658 station-days, each with 96 quarter-hour values.
Normalization: each curve divided by its daily power sum.
KMeans: random_state=42, n_init=10; tested k=2 through 8.
Silhouette: sample_size=1200, random_state=42.
Selected candidate: k=2, sampled silhouette approximately 0.449.
Night window: 22:00-06:00; descriptive, not a tariff definition.
Cluster summaries weight each station-day equally.
Cluster numbers are arbitrary identifiers.
