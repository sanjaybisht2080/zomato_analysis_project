# Zomato Restaurant Data Analysis

Exploratory data analysis of Indian restaurants listed on Zomato, uncovering patterns in ratings, cuisines, pricing, delivery, and restaurant chains across major Indian cities.

## Overview

This project analyzes a dataset of Indian restaurants (`Indian_Resturants.csv`) to answer questions like:

- Which cities have the most restaurants?
- What are the most popular cuisines?
- How does price range relate to customer ratings?
- Which restaurant chains have the widest reach?
- How common is alcohol availability?
- Does delivery availability affect ratings?

## Dataset

The analysis expects a CSV file named `Indian_Resturants.csv` in the project directory, containing restaurant-level fields such as name, city, cuisines, price range, aggregate rating, establishment type, delivery availability, and highlights (amenities/features).

> Note: The dataset itself is not included in this repo — add your own copy of `Indian_Resturants.csv` before running the notebook.

## Data Cleaning

The notebook performs the following preprocessing steps:

- Fills missing values in `address` and `opentable_support`
- Drops unnecessary columns: `zipcode`, `currency`, `latitude`, `longitude`
- Removes duplicate restaurants based on `res_id`
- Drops remaining rows with null values
- Derives a new `alcohol` column (`yes`/`no`) by parsing keywords in the `highlights` column

## Analysis & Visualizations

| Section | What it shows |
|---|---|
| **Rating distribution** | Histogram of `aggregate_rating` across all restaurants |
| **Top cities** | Bar chart of cities with the most restaurants |
| **Popular cuisines** | Bar chart of the most common cuisines |
| **Price vs. rating** | Bar plot comparing average rating across price ranges |
| **Top restaurant chains** | Bar chart of chains with the most outlets |
| **Alcohol availability** | Pie chart of restaurants serving alcohol vs. not |
| **Establishment types** | Count plot of restaurant categories (Quick Bites, Casual Dining, etc.) |
| **Delivery vs. rating** | Stacked bar chart of rating distribution by delivery availability |

## Key Findings

- Ratings cluster mostly between **3.5 and 4.5**, with a peak around 4.0; a spike at 0 suggests many unrated restaurants.
- **Bangalore** has the highest number of listed restaurants, followed by Mumbai and Pune.
- **North Indian** cuisine is by far the most common, followed by fast food and Chinese.
- Higher price ranges tend to correlate with **higher average ratings**.
- **Domino's Pizza** and **Cafe Coffee Day** are the most widely represented chains.
- Around **93%** of restaurants in the dataset do not serve alcohol.
- **Quick Bites** and **Casual Dining** are the dominant establishment types.

## Tech Stack

- Python 3
- pandas
- numpy
- seaborn
- matplotlib

## Getting Started

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install pandas numpy seaborn matplotlib jupyter
   ```
3. Place `Indian_Resturants.csv` in the project root
4. Launch the notebook:
   ```bash
   jupyter notebook zomato_analysis.ipynb
   ```
5. Run all cells to reproduce the analysis and visualizations

## Project Structure

```
.
├── zomato_analysis.ipynb   # Main analysis notebook
├── Indian_Resturants.csv   # Dataset (not included, add your own)
└── README.md
```

## License

This project is open source and available under the [MIT License](LICENSE).
