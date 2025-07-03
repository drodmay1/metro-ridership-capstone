# DC Metro Rail Ridership Trends (2019–2024)
# by David Rodriguez-Mayorquin

## Overview
This project explores daily ridership data from the Washington, DC Metro Rail system from 2019 through 2024. The goal is to analyze how ridership was affected by the COVID-19 pandemic and evaluate changes in rider behavior over time.

## Project Goals
- Visualize ridership trends by year, month, and weekday
- Compare pre-pandemic, pandemic, and post-pandemic ridership patterns
- Build a simple model to forecast ridership trends
- Summarize insights for transit planning and recovery analysis

## Data Source
Data collected from WMATA’s Ridership Portal:  
[https://www.wmata.com/initiatives/ridership-portal/](https://www.wmata.com/initiatives/ridership-portal/)

Only Metro Rail data was used (Metrobus excluded).

## Tools Used
- Python (Pandas, Matplotlib, Seaborn, Scikit-learn)
- Jupyter Notebooks
- Excel (for initial exploration)
- Overleaf / LaTeX for report writing

## Project Structure
/data → Raw and cleaned datasets
/figures → Visualizations
/notebooks → Jupyter notebooks
/src → Python scripts
/output → Model outputs, exports


## Report
[View my Overleaf Report](https://www.overleaf.com/read/hxkvkcqksdhm#049a99)

## Virtual Environment Setup

# 1. Clone the repository
git clone https://github.com/drodmay1/metro-ridership-capstone.git
cd metro-ridership-capstone

# 2. Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate  # (On Windows: .venv\Scripts\activate)

# 3. Install required dependencies
pip install -r requirements.txt

# 4. Launch Jupyter Notebook
jupyter notebook


