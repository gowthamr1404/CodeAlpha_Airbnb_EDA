# NYC Airbnb – Exploratory Data Analysis (EDA)

**CodeAlpha Internship – Data Analytics – Task 2**

An Exploratory Data Analysis (EDA) project on the New York City Airbnb Open Data (2019) dataset, exploring pricing patterns, room types, borough-wise trends, and listing activity across NYC.

## Overview

This project analyzes ~49,000 Airbnb listings across New York City to understand:
- How prices vary across boroughs and room types
- Which areas have the most Airbnb activity
- Patterns in guest reviews and listing availability
- Outliers and anomalies in pricing and booking behavior

## Dataset

**Source:** New York City Airbnb Open Data (2019) — Kaggle
**File:** `AB_NYC_2019.csv`
**Rows:** ~49,000 listings
**Columns:** 16, including `price`, `room_type`, `neighbourhood_group`, `neighbourhood`, `number_of_reviews`, `availability_365`, and host details.

## Tools & Libraries

- **Python 3**
- `pandas` – data loading, cleaning, and analysis
- `numpy` – numerical operations
- `matplotlib` – data visualization

## Analysis Steps

1. **Data Loading & Inspection** – loaded the dataset and reviewed structure with `.head()`, `.info()`.
2. **Data Cleaning** – checked and handled missing values (`name`, `host_name`, `reviews_per_month`) and duplicates.
3. **Descriptive Statistics** – used `.describe()` to understand price, minimum nights, reviews, and availability distributions.
4. **Outlier Detection** – identified extreme values in `price` (up to $10,000/night) and `minimum_nights` (up to 1250 nights), and filtered them for cleaner analysis.
5. **Price Analysis by Borough** – compared average prices across `neighbourhood_group` (Manhattan, Brooklyn, Queens, Bronx, Staten Island).
6. **Room Type Analysis** – compared listing counts and average prices across `room_type` (Entire home/apt, Private room, Shared room).
7. **Listings Distribution** – examined which boroughs have the highest number of listings.
8. **Correlation Analysis** – explored relationships between price, number of reviews, and availability.

## Key Insights

- Around **10,052 listings (~20%)** have never received a review.
- **[Borough]** has the highest average price per night at approximately **$[value]**, while **[Borough]** is the most affordable.
- **[Room type]** listings are priced significantly higher on average (**$[value]**) compared to other room types.
- **[Borough]** has the highest number of total listings, indicating the most active area for Airbnb hosting in NYC.
- A small number of listings show extreme price outliers (above $[value]/night), which were excluded from average price comparisons for cleaner analysis.

## Repository Structure

```
├── CodeAlpha_Airbnb_EDA.ipynb   # Jupyter notebook with full EDA
├── AB_NYC_2019.csv              # Dataset used for analysis
└── README.md                    # Project documentation
```

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/CodeAlpha_Airbnb_EDA.git
   cd CodeAlpha_Airbnb_EDA
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib
   ```
3. Open and run the notebook:
   ```bash
   jupyter notebook CodeAlpha_Airbnb_EDA.ipynb
   ```

## Key Learnings

- Handling missing values and duplicates in real-world datasets
- Identifying and treating outliers before drawing conclusions
- Using `groupby()` for category-wise comparisons
- Creating clear, labeled visualizations with `matplotlib`
- Translating raw statistics into meaningful business insights

## Author

**Gowtham R**
Internship Task – CodeAlpha (Data Analytics)

---
*This project was built as part of the CodeAlpha Data Analytics internship program.*
