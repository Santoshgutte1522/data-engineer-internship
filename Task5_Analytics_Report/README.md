# Task 5: Analytics Report & Insights Documentation

**NYC Yellow Taxi Business Analysis (August 2026)**

## Business objective
Help a taxi fleet operations manager increase revenue per car-hour by finding when, where and on which trips the fleet earns the most.

## Data
- NYC TLC Yellow Taxi Trip Records, August 2026 (3,336,716 raw trips, 3,134,641 after cleaning)
- NYC TLC Taxi Zone Lookup (265 zones)
- Both files are downloaded directly by the notebook from the official TLC website, so no data file is stored here.

## What I did
1. Cleaned the data (removed impossible distances, fares, durations and duplicates; 6.06% removed)
2. Defined KPIs: trips, revenue, revenue per trip, per mile and per minute, tip %, card share, airport share
3. Analysed demand by hour, weekday, zone, borough, trip distance, payment method and airport trips
4. Made 8 charts and wrote business insights and recommendations

## Key findings
- Evening (17:00 to 22:59) has 35.7% of trips, and Saturday 18:00 is the busiest slot of the week
- Revenue per trip-minute is best at 05:00 ($2.05) and worst at 15:00 ($1.60)
- Airport trips are 9.2% of trips but 23.1% of revenue ($2.07 vs $1.66 per minute)
- Manhattan has 87.0% of pickups and 74.5% of revenue; the top 10 zones give 40.5% of revenue
- Trips of 5+ miles are 21.9% of trips but 42.4% of revenue
- 26.2% of trips are Flex Fare with almost no tip recorded, so tip analysis covers card trips only

## Files
| File | Description |
|---|---|
| `Task5_Analytics_Report.ipynb` | Google Colab notebook with code, outputs and charts |
| `Task5_Report.docx` | Full report: executive summary, analysis, insights, recommendations |

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn, Google Colab
