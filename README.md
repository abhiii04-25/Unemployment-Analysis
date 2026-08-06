# Unemployment-Analysis
Analyzes unemployment rate data in India, cleans and explores it, visualizes trends, and quantifies the impact of COVID-19 on unemployment across states and regions.

# 📊 Unemployment Analysis with Python

## 📌 Project Overview
This project analyzes unemployment rate data using Python to identify trends, patterns, and the impact of the COVID-19 pandemic on employment. The analysis includes data cleaning, exploratory data analysis (EDA), visualizations, and insights that can help understand unemployment trends and support informed economic decisions.

---

## 🎯 Objectives
- Analyze unemployment rate data.
- Clean and preprocess the dataset.
- Explore unemployment trends over time.
- Investigate the impact of COVID-19 on unemployment.
- Identify seasonal or regional patterns.
- Present insights through visualizations.

---

## 📂 Dataset
Two datasets are used, both containing:
- Date
- Region / State
- Estimated Unemployment Rate (%)
- Estimated Employed
- Estimated Labour Participation Rate (%)
- Area (Urban/Rural) or Zone (North/South/East/West/Northeast)

| File | Coverage | Notes |
|---|---|---|
| `Unemployment in India.csv` | May 2019 – Jun 2020, 28 states/UTs | Includes Rural/Urban split; long enough to cover pre-COVID and COVID periods |
| `Unemployment_Rate_upto_11_2020.csv` | Jan – Oct 2020, 27 regions | Includes geographic zone, longitude/latitude |

**Source:** Dataset provided for the CodeAlpha Data Science Internship Task.

---

## 🛠 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- ReportLab (PDF report generation)

---

## 📚 Project Workflow

### 1. Import Libraries
Pandas, NumPy, Matplotlib, Seaborn.

### 2. Load Dataset
Read both CSV files and inspect their structure.

### 3. Data Cleaning
- Strip whitespace from column names and string values (the raw files have leading spaces in headers).
- Drop 28 fully-empty trailing rows present in `Unemployment in India.csv`.
- Convert `Date` to `datetime`.
- Rename the duplicated `Region` column in the 2020 file to `Zone`.
- Drop duplicate records.

### 4. Exploratory Data Analysis (EDA)
- Statistical summary
- Correlation analysis between unemployment rate, employed count, and labour participation
- Distribution of unemployment rates
- Monthly national trend

### 5. Data Visualization
- Line chart — monthly unemployment trend
- Bar chart — state-wise and zone-wise average unemployment rate
- Histogram — distribution of unemployment rate
- Box plot — rural vs. urban unemployment
- Correlation heatmap

### 6. COVID-19 Impact Analysis
- Split data into Pre-COVID (before March 2020) and COVID (March 2020 onward) periods.
- Compare national and state-level average unemployment rate between periods.
- Identify the most- and least-affected states.
- Compare labour participation rate before/after.

### 7. Insights & Conclusions
Key findings are printed by the script/notebook and summarized in `report.pdf`.

---

## 📊 Visualizations
Generated automatically in `images/` when you run `analysis.py` or the notebook:
- `unemployment_trend.png` — national monthly trend with COVID marker
- `statewise_unemployment.png` — average unemployment rate by state
- `zonewise_unemployment.png` — average unemployment rate by zone
- `histogram.png` — distribution of unemployment rate
- `heatmap.png` — correlation heatmap
- `boxplot.png` — rural vs. urban unemployment
- `covid_impact_top10_states.png` — pre- vs. during-COVID comparison, top 10 affected states

---

## 📁 Project Structure
```text
Unemployment-Analysis/
│
├── data/
│   ├── Unemployment in India.csv
│   ├── Unemployment_Rate_upto_11_2020.csv
│   ├── unemployment_main_cleaned.csv      (generated)
│   └── unemployment_2020_cleaned.csv      (generated)
│
├── images/
│   ├── unemployment_trend.png
│   ├── statewise_unemployment.png
│   ├── zonewise_unemployment.png
│   ├── histogram.png
│   ├── heatmap.png
│   ├── boxplot.png
│   └── covid_impact_top10_states.png
│
├── notebook.ipynb
├── analysis.py
├── build_report.py
├── requirements.txt
├── README.md
└── report.pdf
```

---

## ▶️ Installation
Clone the repository:
```bash
git clone https://github.com/your-username/Unemployment-Analysis.git
```

Navigate to the project folder:
```bash
cd Unemployment-Analysis
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Run the analysis (generates cleaned data + all charts):
```bash
python analysis.py
```

Regenerate the PDF report (after running `analysis.py`):
```bash
pip install reportlab
python build_report.py
```

Or explore interactively:
```bash
jupyter notebook
```

---

## 📦 Requirements
```text
pandas
numpy
matplotlib
seaborn
jupyter
```
(`reportlab` is additionally required only to rebuild `report.pdf`.)

---

## 📈 Key Findings
- National unemployment rose from **9.51%** (pre-COVID) to **17.77%** during the COVID period — an increase of **8.26 percentage points** — peaking near **24.9%** in May 2020.
- **Puducherry, Tamil Nadu, Jharkhand,** and **Bihar** were hit hardest, each seeing unemployment climb 17–37 percentage points.
- A few regions (Jammu & Kashmir, Tripura, Himachal Pradesh, Chandigarh) saw unemployment ease slightly — the shock was not uniform nationwide.
- The **North** zone carried the highest average unemployment through 2020 (15.89%); the **West** zone was the most resilient (8.24%).
- Labour participation fell alongside rising unemployment (43.89% → 39.33%), suggesting some workers left the labor force entirely rather than remaining active job-seekers.

See `report.pdf` for the full write-up with charts.

---

## 🎓 Learning Outcomes
Through this project, you will gain experience in:
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Visualization
- Time-Series Trend Analysis
- Statistical Interpretation
- Insight Generation
- Python for Data Analysis

---

## 🚀 Future Enhancements
- Build an interactive dashboard using Streamlit.
- Add forecasting models for unemployment trends.
- Create state-wise comparison dashboards.
- Deploy the project as a web application.

---

## 👨‍💻 Author
**Abhishek Sontakke**

MCA (Artificial Intelligence & Machine Learning)

Aspiring AI/ML Engineer | Data Science Enthusiast

---

## ⭐ Support
If you found this project useful, please consider giving it a **⭐ Star** on GitHub.
