# A Study on Sales and Demand Forecasting of Juice Products Using Data Science Techniques

![Python](https://img.shields.io/badge/Python-Data%20Science-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)

## 📌 Project Overview

This project focuses on analyzing historical sales and demand patterns of juice products over the period **2021–2025** using Python-based data analysis and baseline forecasting techniques.

The project was developed as part of a postgraduate academic project in the business context of **Podaran Foods India Pvt. Ltd.** The analysis examines sales trends, seasonal variations, product performance, regional demand, bottle-size preferences, and relationships among selected business variables.

The project demonstrates a complete data analysis workflow, from loading and preparing annual datasets to exploratory analysis, visualization, correlation analysis, and forecasting.

> **Data Note:** This project does not use confidential company sales records. The dataset is based on secondary information and a synthetic sales dataset developed for academic analysis using observed business parameters and project requirements.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze historical sales performance of juice products.
- Identify sales and demand patterns across different time periods.
- Study regional, product, bottle-size, and seasonal variations.
- Examine relationships between production quantity, sales quantity, marketing spend, and other variables.
- Apply baseline forecasting techniques to understand future sales patterns.
- Generate meaningful insights from historical sales data.
- Demonstrate the application of Python-based data science techniques to a business problem.

---

## 📊 Dataset

The project covers sales data for five years:

- **2021**
- **2022**
- **2023**
- **2024**
- **2025**

The project uses five annual CSV files:

```text
podaran_21.csv
podaran_22.csv
podaran_23.csv
podaran_24.csv
podaran_25.csv
```

### Dataset Variables

The dataset contains the following major variables:

| Column | Description |
|---|---|
| `Date` | Date associated with the sales record |
| `Product_Name` | Name of the juice product |
| `Bottle_Size` | Bottle/package size |
| `Region` | Sales region |
| `Production_Quantity` | Quantity produced |
| `Sales_Quantity` | Quantity sold |
| `Price` | Product price |
| `Revenue` | Revenue generated |
| `Marketing_Spend` | Marketing expenditure |
| `Customer_Rating` | Customer rating |

The datasets are loaded separately and then consolidated into a single DataFrame for analysis.

---

## 🧰 Technologies & Tools

### Programming

- Python

### Data Analysis

- Pandas
- NumPy

### Data Visualization

- Matplotlib
- Seaborn

### Development Environment

- Jupyter Notebook

### Data Format

- CSV

---

## 🔄 Project Workflow

```text
Data Collection
       ↓
Annual CSV Files
       ↓
Data Loading
       ↓
Data Consolidation
       ↓
Data Cleaning & Preprocessing
       ↓
Exploratory Data Analysis
       ↓
Time-Based Analysis
       ↓
Correlation Analysis
       ↓
Forecasting
       ↓
Business Insights
```

---

## 🧹 Data Preparation & Preprocessing

The following preprocessing steps were performed:

1. Loaded the five annual CSV datasets using Pandas.
2. Combined the datasets into a single DataFrame.
3. Converted the `Date` column into datetime format.
4. Sorted the records chronologically.
5. Prepared the date field for time-based analysis.
6. Created a working copy of the dataset.
7. Set the date field as an index for time-oriented analysis.
8. Used descriptive statistics to understand the data.

### Example Data Preparation Workflow

```python
import pandas as pd

df1 = pd.read_csv("podaran_21.csv")
df2 = pd.read_csv("podaran_22.csv")
df3 = pd.read_csv("podaran_23.csv")
df4 = pd.read_csv("podaran_24.csv")
df5 = pd.read_csv("podaran_25.csv")

df = pd.concat(
    [df1, df2, df3, df4, df5],
    ignore_index=True
)

df["Date"] = pd.to_datetime(df["Date"])
df = df.sort_values("Date")

df_copy = df.copy()
df_copy.set_index("Date", inplace=True)

print(df_copy.info())
print(df_copy.describe())
```

---

# 🔍 Exploratory Data Analysis

The project performs exploratory analysis from multiple perspectives.

## 1. Weekly Sales Analysis

Weekly sales patterns were analyzed to understand short-term fluctuations and changes in sales activity.

## 2. Monthly Sales Analysis

Monthly sales trends were examined to identify changes in demand across months.

## 3. Yearly Sales Analysis

Yearly sales performance was analyzed to understand long-term changes across the 2021–2025 study period.

## 4. Region-wise Sales Analysis

Sales were compared across regions to identify major contributing markets.

## 5. Product-wise Sales Analysis

Different juice products were compared to identify high-performing products.

## 6. Bottle-size Analysis

The distribution of sales across bottle sizes was examined to understand packaging preferences.

## 7. Seasonal Analysis

Sales patterns were studied across seasons to identify demand variations during different periods of the year.

## 8. Marketing Spend vs Sales

The relationship between marketing expenditure and sales performance was analyzed.

## 9. Correlation Analysis

Correlation analysis was performed to understand relationships among numerical variables.

---

# 📈 Visualizations

The project includes the following visualizations:

- Weekly Sales Trend
- Monthly Sales Trend
- Yearly Sales Trend
- Region-wise Sales
- Product-wise Sales
- Bottle-size Distribution
- Seasonal Analysis
- Marketing Spend vs Sales
- Correlation Heatmap
- Moving Average Forecast
- Trend Forecast
- Cumulative Sales Trend
- Yearly Growth Analysis

---

# 🔮 Forecasting

This project uses **baseline forecasting approaches** to study future sales patterns.

## Moving Average Forecast

Moving-average analysis is used to smooth short-term fluctuations in sales data and highlight the underlying movement of the series.

The moving average provides a simpler representation of the historical pattern and helps reduce the effect of short-term variation.

## Trend Forecast

Trend analysis is used to examine the overall direction of sales over time.

The trend analysis helps determine whether sales show an overall upward or downward movement throughout the study period.

> **Note:** These are baseline forecasting techniques used for the academic project. They are not intended to represent official future sales forecasts for Podaran Foods.

---

# 📊 Key Findings

The analysis produced the following observations from the project dataset:

- **Tamil Nadu and Kerala** were identified as major sales regions.
- **Mango and Cola** were identified as high-selling products.
- **200 ml** was identified as the leading bottle size.
- Higher sales were observed during the **summer period**, indicating seasonal variation.
- Marketing spend showed a **weak-to-moderate positive relationship** with sales.
- The highest reported correlation in the analysis was **0.98 between production quantity and sales quantity**.
- Moving-average analysis helped smooth short-term fluctuations.
- Trend analysis showed an overall upward movement in sales.
- Cumulative sales showed an increasing pattern across the study period.
- Year-over-year growth was analyzed to understand annual changes in sales.

---

# 📌 Business Interpretation

The analysis demonstrates how historical sales data can be used to understand:

- Demand patterns
- Product performance
- Regional sales contribution
- Seasonal variations
- Packaging preferences
- Production and sales relationships
- Marketing and sales relationships
- Long-term sales trends

The findings provide an analytical view of the dataset and demonstrate how data science techniques can support business-oriented sales and demand analysis.

---

# 📁 Repository Structure

```text
podaran-sales-demand-forecasting/
│
├── README.md
├── requirements.txt
│
├── notebooks/
│   └── Podaran_Sales_Demand_Forecasting.ipynb
│
├── data/
│   ├── README.md
│   └── sample/
│       ├── podaran_21_sample.csv
│       ├── podaran_22_sample.csv
│       ├── podaran_23_sample.csv
│       ├── podaran_24_sample.csv
│       └── podaran_25_sample.csv
│
├── visuals/
│   ├── weekly_sales_trend.png
│   ├── monthly_sales_trend.png
│   ├── yearly_sales_trend.png
│   ├── region_wise_sales.png
│   ├── product_wise_sales.png
│   ├── bottle_size_distribution.png
│   ├── seasonal_analysis.png
│   ├── marketing_spend_vs_sales.png
│   ├── correlation_heatmap.png
│   ├── moving_average_forecast.png
│   ├── trend_forecast.png
│   ├── cumulative_sales.png
│   └── yearly_growth.png
│
└── report/
    └── project_summary.pdf
```

---

# ▶️ How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/Praveen-086/podaran-sales-demand-forecasting.git
```

## 2. Navigate to the Project Directory

```bash
cd podaran-sales-demand-forecasting
```

## 3. Install Required Libraries

```bash
pip install -r requirements.txt
```

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

## 5. Open the Notebook

Navigate to:

```text
notebooks/Podaran_Sales_Demand_Forecasting.ipynb
```

## 6. Run the Notebook

Run the cells sequentially to reproduce:

- Data loading
- Data consolidation
- Data preprocessing
- Exploratory data analysis
- Visualizations
- Correlation analysis
- Forecasting
- Key findings

---

# 📦 Requirements

The project requires the following Python libraries:

```text
pandas
numpy
matplotlib
seaborn
jupyter
```

These can be installed using:

```bash
pip install -r requirements.txt
```

---

# 📚 Project Documentation

The repository is based on a postgraduate academic project titled:

> **A Study on Sales and Demand Forecasting of Juice Products Using Data Science Techniques at Podaran Foods India Pvt Ltd**

The academic study covers the period **2021–2025** and applies Python-based data analysis, visualization, statistical analysis, and baseline forecasting techniques.

---

# ⚠️ Data Disclaimer

This repository is created for **academic, learning, and portfolio purposes**.

The project was developed in the business context of **Podaran Foods India Pvt. Ltd.**, but confidential company sales records were **not used**.

The dataset used in the project consists of **secondary information and a synthetic sales dataset prepared for analytical and academic purposes** based on observed business parameters and project requirements.

Therefore:

- The dataset should not be considered official company data.
- The findings should not be interpreted as official company performance figures.
- The forecasts should not be interpreted as official future sales projections.
- The project is intended to demonstrate data analysis and forecasting techniques.

---

# 🚧 Limitations

- The analysis is based on secondary/synthetic data rather than confidential company sales records.
- The forecasting methods used are baseline methods such as moving average and trend analysis.
- External demand factors are not comprehensively modeled.
- Weather, holidays, competitor activity, distribution changes, and other external factors are not fully incorporated.
- The results are intended for academic and portfolio demonstration.

---

# 🔮 Future Improvements

The project can be extended using more advanced approaches such as:

- Advanced time-series forecasting models
- Machine-learning-based demand prediction
- Feature engineering using external variables
- Holiday and seasonal event analysis
- Weather-related demand factors
- Promotional campaign analysis
- Inventory and stock optimization
- Automated forecasting pipelines
- Interactive dashboard integration using Power BI
- Deployment as a web-based analytics application

---

# 👨‍💻 Author

## Praveen Kumar R

**M.Com. – Finance and Computer Applications**  
Bharathiar University

### Areas of Interest

- Data Science
- Machine Learning
- Artificial Intelligence
- Data Analytics
- Predictive Analytics

### 🔗 Connect with Me

**LinkedIn:**  
https://www.linkedin.com/in/r-praveen-kumar-082k4

**GitHub:**  
https://github.com/Praveen-086

---

# ⭐ Project Highlights

| Item | Details |
|---|---|
| Study Period | 2021–2025 |
| Domain | Beverage / FMCG Sales |
| Analysis Type | Sales & Demand Analysis |
| Forecasting | Moving Average & Trend Analysis |
| Programming | Python |
| Libraries | Pandas, NumPy, Matplotlib, Seaborn |
| Environment | Jupyter Notebook |
| Data Format | CSV |

---

## 📌 Project Status

**Status:** Completed Academic Project

The repository contains the analytical workflow, notebook, visualizations, documentation, and selected sample data required to understand and reproduce the project.
