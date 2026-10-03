# Python: Sales Data Analysis

Exploratory analysis of daily sales data for January – August 2018, including outlier detection, top-product analysis, and a comparison of sales with weather data for Astana.

## Data
**`data.csv`**: 301,355 rows of sales records (04.01.2018 – 31.08.2018)
| Column | Description |
|---|---|
| `Дата` | Sale date |
| `Склад` | Warehouse number (5 warehouses) |
| `Контрагент` | Customer / delivery address (211 unique) |
| `Номенклатура` | Product (24 unique) |
| `Количество` | Quantity sold |

**`weather.csv.gz.csv`**: weather archive for Astana from [rp5.ru](https://rp5.ru/Архив_погоды_в_Астане), converted to the date and average daily temperature (`T`)

## Tasks
1. Load the data and check column types (convert `Дата` to datetime)
2. Group the data by date and count total sales per day
3. Plot daily sales and describe the chart
4. Find the row with the largest outlier in quantity sold
5. Find the top product sold on Wednesdays in June–August at warehouse 3
6. Load the weather data, calculate the average daily temperature, merge it with daily sales, and plot sales vs temperature plus a separate temperature chart

## Key Findings
- **Trend:** sales grow from winter to summer, from ≈3,716/day in January to ≈5,016/day in August, with a sharp jump (~20%) in May
- **Weekly seasonality:** there are no sales on Mondays; Tuesday is the peak (≈4,911 on average) and Saturday is the weakest day (≈3,978)
- **Daily stats:** mean ≈ 4,339, median ≈ 4,319, std ≈ 648
- **Largest outlier:** 28.06.2018, warehouse 1, `address_208`, `product_0`, quantity **200**
- **Top product (Wednesdays, Jun–Aug, warehouse 3):** `product_1` with **2,267** units
- **Weather:** sales rise as the temperature rises from winter to summer

## Tools
Python, pandas, NumPy, matplotlib, seaborn, Jupyter Notebook

## Files
- `FINAL_PYTHON_BLOCK3.ipynb`: notebook with code, answers, and charts
- `data.csv`: sales dataset
- `weather.csv.gz.csv`: Astana weather data from rp5.ru

## How to Run
1. Install the libraries:
   `pip install pandas numpy matplotlib seaborn jupyter`
2. Put `data.csv` and `weather.csv.gz.csv` in the same folder as the notebook
3. Open and run `FINAL_PYTHON_BLOCK3.ipynb`
