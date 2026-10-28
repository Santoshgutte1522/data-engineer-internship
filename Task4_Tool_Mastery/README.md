# Task 4: Data Science Tool Mastery Project

Data Engineer Internship, Task 4.

## Project
SQL, Plotly and scikit-learn applied to earthquake data for India and nearby regions (2000 to 2026).

## Tools
| Tool | Used for |
|------|----------|
| SQL (SQLite) | 8 queries: filtering, GROUP BY, HAVING, CASE WHEN, subquery, CTE, RANK, running total (SUM OVER) and LAG |
| Plotly Express | 6 interactive charts: map, stacked bar, sunburst, box plot, density heatmap, animated map by year |
| scikit-learn | KMeans clustering into 6 seismic zones, and a deep vs shallow classifier (Logistic Regression and Random Forest vs a baseline) |
| Pandas, NumPy | Loading and preparing the data |
| Google Colab | Running everything |

## Data
Cleaned USGS earthquake data (15,381 rows) from Task 3. The notebook loads it from the `Task3_Earthquake_Analysis` folder of this repository.

## Files
| File | Description |
|------|-------------|
| `Task4_Tool_Mastery.ipynb` | Colab notebook with all code, outputs and interactive charts |
| `Task4_Report.docx` | Written report with results and charts |

## How to run
1. Open the notebook in Google Colab (the Plotly charts are interactive there).
2. Click Runtime > Run all.
3. Libraries: pandas, numpy, plotly, scikit-learn (already in Colab). SQLite comes with Python.

## Key results
- India has the most earthquakes (5,073); Afghanistan has the deepest (average 143.4 km)
- By the end of 2005, 30% of all earthquakes in the 27 years had been recorded (aftershock sequences)
- KMeans found 6 zones; only the Hindu Kush zone is deep (average 115 km)
- Random Forest predicts deep vs shallow with 94.5% accuracy (baseline 72.6%); 94.2% on a time-based test (baseline 66.5%)
- The model works from location (latitude and longitude), not magnitude. It is not an earthquake predictor.

Note: GitHub's notebook preview may show the Plotly charts as blank. Open the notebook in Colab to see them.
