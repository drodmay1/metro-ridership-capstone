# 🚇 DC Metro Rail Ridership Trends (2019–2024)  
**by David Rodriguez-Mayorquin**

## Overview
This project explores daily ridership data from the Washington, DC Metro Rail system from 2019 through 2024. The goal is to analyze how ridership was affected by the COVID-19 pandemic and evaluate changes in rider behavior over time.

## Project Goals
- Visualize ridership trends by year, month, and weekday
- Compare pre-pandemic, pandemic, and post-pandemic ridership patterns
- Build a simple model to forecast ridership trends
- Summarize insights for transit planning and recovery analysis

## Data Source
Data collected from WMATA’s Ridership Portal:  
🔗 [WMATA Ridership Portal](https://www.wmata.com/initiatives/ridership-portal/)

Only Metro Rail data was used (Metrobus excluded).

## Tools Used
- Python (Pandas, Matplotlib, Seaborn, Scikit-learn)
- Jupyter Notebooks
- Excel (for initial exploration)
- Overleaf / LaTeX for report writing

## Repository Structure

```
metro-ridership-capstone/
├── .venv/                        # Virtual environment (ignored by Git)
├── data/                         # Raw and cleaned data files (CSV, XLSX)
│   ├── Capstone_Diagram.drawio.png
│   ├── clean_metroridership.csv
│   ├── daily_metrorail_ridership.xlsx
│   └── metroridership.csv
├── notebooks/                    # Jupyter notebooks
│   ├── 01_data_overview.ipynb
│   └── 02_data_description.ipynb
├── figures/                      # Exported chart images (PNG)
├── .gitignore                    # Files and folders to ignore in Git
├── requirements.txt              # Project dependencies
└── README.md                     # Project overview and setup instructions

```

## Advanced Analysis: Predictive Modeling

To explore future ridership trends, I trained and evaluated four machine learning models using features derived from the Metrorail ridership dataset:

- **Linear Regression**
- **Random Forest Regressor**
- **Support Vector Regression (SVR)**
- **Gradient Boosting Regressor**

### Features Used
- Year
- Month
- Day of Week
- Is Weekend
- Is Holiday

The dataset was split into training and testing sets using an 80/20 ratio. Models were evaluated using **Mean Squared Error (MSE)** and **R² (coefficient of determination)**.

### Results Summary

| Model                  | MSE           | R² Score |
|------------------------|---------------|----------|
| Linear Regression      | 52,116,658,235 | -4.2185  |
| Random Forest Regressor| 1,951,757,714  | 0.9507   |
| Support Vector Regressor| 3,532,779,314 | 0.8982   |
| Gradient Boosting      | 4,983,145,736  | 0.8740   |

Random Forest achieved the best performance in terms of both accuracy and generalization.

See full code in [01_data_overview.ipynb](notebooks/01_data_overview.ipynb)

## Key Visuals
### Modeling Pipeline
![Modeling Diagram](data/Capstone_Diagram.drawio.png)

### Sample EDA Visualizations  
**1. Average Ridership by Day of Week**  
![Avg by Day of Week](figures/eda_avg_by_day_of_week.png)

**2. Daily Ridership Distribution**  
![Daily Ridership](figures/eda_distribution_daily_ridership.png)

**3. Holiday vs No Holiday Ridership**  
![Holiday vs No Holiday](figures/eda_holiday_vs_noholiday.png)

**4. Monthly Averages**  
![Monthly Avg](figures/eda_monthly_average.png)

**5. Seasonality Across Years**  
![Seasonality Across Years](figures/eda_monthly_seasonality_acrossyears.png)

**6. Moving Average Trendline**  
![Moving Avg](figures/eda_moving_avg_trendline.png)

**7. Monthly Trends (2019–2024)**  
![Month-to-Month](figures/eda_seasonal_trend_month_to_month.png)

**8. Total Ridership by Year**  
![Yearly Total](figures/eda_total_ridership_by_year.png)

**9. Post-COVID Weekday Trends**  
![Post COVID](figures/eda_weekday_avg_postcovid.png)


## Report
[View my Overleaf Report](https://www.overleaf.com/read/hxkvkcqksdhm#049a99)

## Virtual Environment Setup

```bash
# 1. Clone the repository
git clone https://github.com/drodmay1/metro-ridership-capstone.git
cd metro-ridership-capstone

# 2. Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate  # (On Windows: .venv\Scripts\activate)

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter Notebook
jupyter notebook





