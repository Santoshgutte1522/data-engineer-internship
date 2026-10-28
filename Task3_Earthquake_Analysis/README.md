# Task 3: Real-World Dataset Analysis Project

Data Engineer Internship, Task 3.

## Project
Earthquake Activity in India and Nearby Regions, 2000 to 2026.

## Dataset
- Source: USGS Earthquake Catalog (United States Geological Survey), https://earthquake.usgs.gov/fdsnws/event/1/
- Region: latitude 6 to 37, longitude 68 to 98 (India, Himalayas and neighbouring countries)
- Filter: magnitude 4 and above, 1 Jan 2000 to 27 Oct 2026
- Raw data: 15,383 rows, 22 columns. Clean data: 15,381 rows.

## What this covers
- Downloading real data from an official API
- Data exploration: missing values, duplicates, data types, categories
- Data cleaning: removed non-earthquake events, fixed labels, dropped mostly empty columns, merged country names
- Exploratory data analysis: country summary, correlation, seasonality, Gutenberg-Richter law
- 8 visualizations: line chart, bar chart, histograms, map-style scatter plot, box plot, scatter plot, heatmap, log-scale plot
- Insights, recommendations and limitations

## Files
| File | Description |
|------|-------------|
| `Task3_Earthquake_Analysis.ipynb` | Colab notebook with all code, outputs and charts |
| `Task3_Report.docx` | Written report |
| `india_earthquakes_raw.csv` | Raw data downloaded from USGS |
| `india_earthquakes_clean.csv` | Cleaned data used for the analysis |

## How to run
1. Open the notebook in Google Colab.
2. Run all cells from top to bottom (the first cell downloads the data from USGS).
3. Libraries: pandas, numpy, matplotlib, seaborn (already in Colab).

## Key results
- 15,381 earthquakes, median 459 per year
- India has the most (5,073), with about 43% near Port Blair and Bamboo Flat (Andaman and Nicobar)
- The 2004 and 2005 spike is caused by aftershock sequences, not a trend
- 72.6% of earthquakes are shallow (under 70 km)
- Gutenberg-Richter b-value: 1.08
